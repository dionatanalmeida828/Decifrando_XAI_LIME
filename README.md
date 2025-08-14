# Decifrando a Caixa Preta: Exemplo de modelo de crédito com LIME

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score
import lime
import lime.lime_tabular

# Carregar dataset
# Se você tiver o CSV, coloque o caminho correto
dataset_path = 'dataset.csv'
data = pd.read_csv(dataset_path)

# Separar features e target
X = data.drop('target', axis=1)  # Substitua 'target' pelo nome da coluna do risco
y = data['target']

# Dividir em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Treinar modelo
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Avaliar modelo
y_pred = model.predict(X_test)
print("Acurácia:", accuracy_score(y_test, y_pred))

# Aplicar LIME
explainer = lime.lime_tabular.LimeTabularExplainer(
    training_data=X_train.values,
    feature_names=X_train.columns,
    class_names=['Baixo Risco', 'Alto Risco'],
    mode='classification'
)

# Explicação para o primeiro cliente de teste
i = 0
exp = explainer.explain_instance(X_test.values[i], model.predict_proba, num_features=5)
exp.show_in_notebook(show_table=True)


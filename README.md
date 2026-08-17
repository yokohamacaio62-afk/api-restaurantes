API Restaurantes

API desenvolvida em FastAPI que consome dados de cardápios de redes de fast-food (McDonald's, Burger King, KFC, Taco Bell, Wendy's, Pizza Hut) a partir de uma fonte externa e disponibiliza endpoints para consulta.

🚀 Tecnologias
Python
FastAPI
Uvicorn
Requests
📦 Instalação

Clone o repositório:

bash
git clone https://github.com/yokohamacaio62-afk/api-restaurantes.git
cd api-restaurantes

Crie e ative um ambiente virtual:

bash
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # Linux/Mac

Instale as dependências:

bash
pip install -r requirements.txt
▶️ Como rodar
bash
uvicorn main:app --reload

A API ficará disponível em http://127.0.0.1:8000.

Documentação interativa (Swagger): http://127.0.0.1:8000/docs

📍 Endpoints
GET /api/hello

Endpoint de teste.

GET /api/restaurantes/

Retorna o cardápio dos restaurantes.

Parâmetro opcional:

restaurante (string): filtra o cardápio por nome do restaurante (ex: McDonald's, Burger King, KFC, Taco Bell, Wendy's, Pizza Hut)

Exemplo:

GET /api/restaurantes/?restaurante=Pizza Hut

Resposta:

json
{
  "Restaurante": "Pizza Hut",
  "Cardapio": [
    {
      "item": "Detroit Double Cheesy Pizza Slice",
      "price": 57.06,
      "description": "Sinta o sabor do verão a cada gole."
    }
  ]
}
📁 Estrutura do projeto
├── main.py          # Aplicação FastAPI com os endpoints
├── app.py           # Script para consumir a API externa e gerar arquivos JSON por restaurante
├── requirements.txt # Dependências do projeto
└── *.json           # Cardápios gerados por restaurante
✍️ Autor

Caio Yokohama

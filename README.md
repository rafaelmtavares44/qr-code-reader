QR Code Reader - Dashboard BI
Aplicação desenvolvida em Python com Streamlit para leitura e extração da chave de acesso fiscal (NFC-e) a partir de QR Codes de cupons fiscais. O sistema permite leitura por imagem ou webcam, evita duplicidades e organiza as chaves em um arquivo CSV, pronto para análises em Business Intelligence.

🧭 Objetivo do Projeto
Este projeto foi desenvolvido para a disciplina de Business Intelligence com o objetivo de:

Automatizar a coleta de chaves fiscais via QR Code.

Eliminar erros e duplicidades na entrada de dados.

Centralizar as informações fiscais para análises em dashboards.

Simular um processo real de captura de dados de vendas no varejo.

🏗️ Arquitetura e Funcionalidades
Principais recursos da aplicação:

Leitura via Webcam: Captura QR Codes em tempo real.

Upload de Imagem: Permite processar imagens de notas fiscais.

Extração automática: Utiliza expressões regulares para identificar a chave fiscal (44 dígitos).

Armazenamento: Salva os dados em .csv com data e hora de captura.

Controle de duplicidade: Impede registro repetido da mesma chave.

Interface Web: Desenvolvida com Streamlit, de fácil uso e visualização.

📂 Estrutura do Projeto
text
📁 QR CODE READER
├── BI.py                # Código principal da aplicação
├── requirements.txt     # Dependências do projeto
├── README.md            # Documentação completa
└── /venv/               # Ambiente virtual (não incluído no GitHub)
⚙️ Tecnologias Utilizadas
Python 3.13

Streamlit – Interface web

OpenCV e pyzbar – Leitura de QR Code

Pandas – Manipulação e exportação de dados

Pillow (PIL) – Processamento de imagem

Regex (re) – Extração da chave fiscal

🚀 Executando o Projeto
Clone o repositório:

bash
git clone https://github.com/SEU_USUARIO/qr-code-reader.git
cd qr-code-reader
Crie e ative o ambiente virtual:

bash
python -m venv venv
.\venv\Scripts\activate
Instale as dependências:

bash
pip install -r requirements.txt
Execute o aplicativo:

bash
streamlit run BI.py
Acesse no navegador:
http://localhost:8501

🧩 Estrutura do Código
Funções principais:

Função	Descrição
load_existing_keys()	Carrega chaves existentes do CSV
save_to_csv()	Salva nova chave com data/hora
extract_access_key()	Extrai a chave fiscal do QR
process_uploaded_image()	Lê e processa imagem enviada
decode_qr_from_frame()	Faz leitura ao vivo pela webcam
📊 Exemplo do Resultado
Após a leitura bem-sucedida, o sistema gera um arquivo access_keys.csv com o seguinte formato:

access_key	timestamp
52250339346861034147651070004999491107141815	2025-10-14 19:43:05
51080167830456000185550010000000031000000030	2025-10-14 19:47:54
📈 Aplicações Futuras
Conexão com bancos de dados SQL.

Integração com dashboards BI (Power BI ou Streamlit Charts).

Leitura de PDFs fiscais com notas em lote.

Interface multilíngue e suporte móvel.

👨‍💻 Equipe de Desenvolvimento
Faculdade: SENAI FATESG
Curso: Inteligência Artificial
Disciplina: Business Intelligence
Docente: Ms. Ujeverson Tavares Sampaio

Integrantes:

Rafael Machado, Bruno Matheus, Jorge Vinícius, José Pazian

[Demais nomes do grupo, se houver]

📜 Licença
Este projeto foi desenvolvido apenas para fins educacionais.

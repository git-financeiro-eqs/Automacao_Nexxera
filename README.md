# Automação Nexxera

## 📌 Descrição
Este script automatiza o processo de incerção de arquivos CNAB no microsiga. A automação faz isso coletando esses arquivos na plataforma **Nexxera WebEDI**, extraindo dados do nome dos arquivos e, destinando-os corretamente no **Microsiga** a partir destes dados.
A automação garante que os arquivos sejam baixados, descompactados e lançados corretamente no sistema.

---

## 🚀 Tecnologias Utilizadas
- **Python 3**
- **Selenium** → Automação de navegador  
- **PyAutoGUI** → Automação de teclado e mouse  
- **EasyOCR** → Reconhecimento óptico de caracteres  
- **Shutil & ZipFile** → Manipulação de arquivos  
- **WebDriver Manager** → Gerenciamento do ChromeDriver  
- **Pathlib & OS** → Operações com diretórios  

---

## ⚙️ Funcionalidades
✅ Acessa a plataforma **Nexxera WebEDI** e realiza login automaticamente  
✅ Filtra os arquivos disponíveis por **período específicado**  
✅ Baixa e **descompacta** os arquivos CNAB  
✅ Lança os arquivos no **ERP Microsiga**  
✅ Utiliza **OCR** para garantir a correta **data de lançamento**  

---

## 🛠️ Como Usar

### Instalação:

1️. Clone o repositório ou baixe o arquivo ZIP do programa:
```bash
https://github.com/git-financeiro-eqs/Automacao_Nexxera.git
```
2. Instale as dependências
```bash
pip install -r requirements.txt
```
2️. Execute o script:
```bash
python gui.py
```
3️. Informe o período desejado na interface da automação.

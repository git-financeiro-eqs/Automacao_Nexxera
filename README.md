# 📂 Automação Nexxera

## 📌 Descrição
Este script automatiza o processo de login, extração e processamento de arquivos CNAB a partir da plataforma **Nexxera WebEDI**, transferindo os dados para o **ERP Microsiga**.  
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
✅ Filtra os arquivos disponíveis por **período específico**  
✅ Baixa e **descompacta** os arquivos CNAB  
✅ Lança os arquivos no **ERP Microsiga**  
✅ Utiliza **OCR** para garantir a correta **data de lançamento**  

---

## 🛠️ Como Usar

### 1️⃣ Instale as dependências:

```bash
pip install -r requirements.txt
```
2️⃣ Execute o script:
```bash
python gui.py
```
3️⃣ Informe o período desejado quando solicitado.

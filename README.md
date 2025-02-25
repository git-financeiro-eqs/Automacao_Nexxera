# Automação Nexxera

## 📌 Descrição
Este script automatiza o processo de incerção de arquivos CNAB no microsiga. A automação faz isso coletando esses arquivos na plataforma **Nexxera SkylineWeb**, extraindo dados do nome dos arquivos e, destinando-os corretamente no **Microsiga** a partir destes dados.
A automação garante que os arquivos sejam baixados, descompactados e lançados corretamente no sistema.

---

## 🚀 Tecnologias Utilizadas
- **Python**
- **Selenium** → Automação de navegador  
- **PyAutoGUI** → Automação de teclado e mouse  
- **EasyOCR** → Reconhecimento óptico de caracteres  
- **Shutil & ZipFile** → Manipulação de arquivos  
- **WebDriver Manager** → Gerenciamento do ChromeDriver  
- **Pathlib & OS** → Operações com diretórios  

---

## ⚙️ Funcionalidades
✅ Acessa a plataforma **Nexxera SkylineWeb** e realiza login automaticamente  
✅ Filtra os arquivos disponíveis por **período específicado**  
✅ Baixa e **descompacta** os arquivos CNAB  
✅ Lança os arquivos no **ERP Microsiga**  
✅ Utiliza **OCR** para garantir a correta **data de lançamento**  

---

## 🛠️ Instalação:

1. Clone o repositório ou baixe o arquivo ZIP do programa:
```bash
https://github.com/git-financeiro-eqs/Automacao_Nexxera.git
```

2. Instale as dependências
```bash
pip install -r requirements.txt
```

3. Execute o script:
```bash
python gui.py
```
<br/>

##  Como Usar

1. O Microsiga precisa estar aberto na tela principal da rotina "Funcões Ctas a Pag".

2. Informe o período desejado na interface da automação.

3. Clique no botão "Acionar" e aguarde até que ela finalize o processo não inserindo mais nenhum arquivo na rotina do Siga.

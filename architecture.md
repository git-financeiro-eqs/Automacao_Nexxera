# 🏗️ Arquitetura do Projeto

Este projeto é uma automação baseada em rapagem de tela por meio das bibliotecas **Selenium** e **PyautoGui** para extração e processamento de arquivos **CNAB** da plataforma **Nexxera SkylineWeb** e integração desse tais documentos no sistema ERP **Microsiga**.  
A automação possui uma arquitetura modular, separando as responsabilidades em três módulos principais para facilitar a manutenção e escalabilidade.  
Seu estilo de codificação segue um modelo **procedural modular**.

---
<br/>


## 📂 Módulos do Projeto
<br/>

| **Módulo**  | **Descrição**  | **Principais Responsabilidades**  |
|-------------|---------------|------------------------------------|
| `gui`       | Módulo responsável pela interface gráfica utilizando **Tkinter**. | - Disponibilizar o botão de acionamento. <br> - Permitir seleção de período. |
| `utils`     | Módulo contendo funções auxiliares reutilizáveis para otimizar a execução. | - Função auxiliar para o processamento dos arquivos CNAB. <br> - Funções de ações repetitivas. |
| `main`   | Script principal da automação, integrando o módulo `utils`. | - Lógica de execução da automação. <br> - Controlar o fluxo de download, extração e envio ao ERP. <br> - Gerenciar exceções e verificar estabilidade do sistema. |

---
<br/>

## 🔍 Fluxo de Execução

1️⃣ **O usuário inicia a automação via interface gráfica (`gui`).**  
2️⃣ **A automação acessa o portal Nexxera e realiza login automaticamente.**  
3️⃣ **Os arquivos CNAB são filtrados pelo período desejado e baixados.**  
4️⃣ **Os arquivos são descompactados e processados (`utils`).**  
5️⃣ **Os dados são lançados no ERP Microsiga (`main.py`).**  
6️⃣ **OCR (`EasyOCR`) é utilizado para validar a data de lançamento.**  

---
<br/>

## 🛠️ Observação Importante

Na rotina "Funcões Ctas a Pag" do Microsiga, por algum motivo que ninguém sabe explicar, dependendo da data de vencimento de um dos títulos que está sendo importado naquele momento através do arquivo CNAB extraído
do portal da Nexxera, a Data Base do sistema muda imprevisivelmente para a data de pagamento daquele título, ou, para alguma data de 2005 (sim, isso é muito estranho e esquisito).
Isso não acontece todas as vezes, mas pode acontecer. Para evitar que isso interfira no processo, criei uma lógica de programação que usa a tecnologia OCR para verificar a Data Base a cada novo lançamento.

---

🚀 **Com essa arquitetura modular, a automação garante organização, escalabilidade e manutenção facilitada.**  

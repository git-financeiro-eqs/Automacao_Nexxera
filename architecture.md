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
| `main`   | Script principal da automação, integrando o módulo `utils`. | - Lógica de execução da automação. |

---
<br/>

## 🛠️ Observação Importante

Na rotina "Funcões Ctas a Pag" do Microsiga, por algum motivo que ninguém sabe explicar, dependendo da data de vencimento de um dos títulos que está sendo importado naquele momento através do arquivo CNAB extraído
do portal da Nexxera, a Data Base do sistema muda imprevisivelmente para a data de pagamento daquele título, ou, para alguma data de 2005 (sim, isso é muito estranho e esquisito).
Isso não acontece todas as vezes, mas pode acontecer. Para evitar que isso interfira no processo, criei uma lógica de programação que usa a tecnologia OCR para verificar a Data Base a cada novo lançamento.
<br/>

Outro ponto importante a se esclarecer é que não seram todos os arquivos extraídos da plataforma Nexxera SkylineWeb dentro do período determinado que seram importados para o sistema Microsiga. Os arquivos que devem ser importados precisam cumprir dois critérios: o arquivo não pode ser de extenção ".protocolo" e precisa ter "PAG" nas três primeiras letras de seu nome, conforme demonstra esse trecho do código:
```
arquivos = [arquivo for arquivo in os.listdir(pasta_destino) if not arquivo.endswith(".protocolo") and arquivo[:3] == "PAG"]
```

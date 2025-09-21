# Desafio de Projeto:  Proposta de Arquitetura de Nuvem na AWS
<p align="center">
  <img alt="Status do Projeto" src="https://img.shields.io/badge/status-concluído-brightgreen">
  <img alt="Último Commit" src="https://img.shields.io/github/last-commit/skyzinha-chan/desafio1_Santander-Code-Girls-2025">
  <img alt="Licença" src="https://img.shields.io/github/license/skyzinha-chan/desafio1_Santander-Code-Girls-2025">
</p>

Este repositório documenta a solução para o Desafio de Projeto do bootcamp **Santander Code Girls 2025**, focado em conceitos de Cloud Computing com a AWS. O objetivo é apresentar uma solução de arquitetura de nuvem utilizando os principais serviços da Amazon Web Services (AWS), conforme solicitado na primeira parte do desafio.

---
## 1. Arquitetura da Solução Proposta

A arquitetura desenhada representa uma aplicação web simples e robusta na nuvem da AWS, onde um usuário interage com uma infraestrutura escalável e segura para enviar e processar arquivos.


### Diagrama

![Diagrama da Arquitetura AWS](https://github.com/skyzinha-chan/desafio1_Santander-Code-Girls-2025/blob/57b7c4224ab26a75052f8f0270a1d09051952cfb/images/desafio1_Santander%20Code%20Girls%20-%202025.png) 

### Descrição dos Componentes

* **Actor (Usuário)**: Representa o cliente final que interage com a aplicação, iniciando o fluxo com o envio de um arquivo.
* **EC2 (Elastic Compute Cloud)**: É o servidor virtual central da nossa aplicação. Ele é responsável por receber as requisições, processar os arquivos enviados e executar a lógica de negócio principal.
* **EBS (Elastic Block Store)**: São os volumes de armazenamento (discos rígidos virtuais) conectados à instância EC2. A arquitetura sugere o uso de múltiplos volumes para uma melhor organização e gerenciamento de dados, como um para o sistema operacional e outros para os dados da aplicação.
A arquitetura utiliza dois volumes:
    * **Volume D-EBS**: Poderia ser utilizado para armazenar os dados brutos ou arquivos da aplicação, separado do sistema operacional para facilitar backups e gerenciamento.
    * **Volume E-EBS**: Poderia funcionar como um volume de backup, para logs ou para dados processados, garantindo maior organização e segurança.
* **RDS (Relational Database Service)**: É o serviço de banco de dados gerenciado da AWS. Ele armazena informações estruturadas, como metadados dos arquivos, perfis de usuário ou logs de transações, de forma segura e escalável, sem a necessidade de gerenciar o servidor de banco de dados manualmente.


### Fluxo da Aplicação

1.  O **Usuário** envia um arquivo para a aplicação.
2.  A instância **EC2** recebe este arquivo.
3.  A lógica da aplicação na **EC2** processa o arquivo e armazena os dados nos volumes **EBS** anexados.
4.  As informações e metadados relevantes sobre o arquivo ou a operação são gravados no banco de dados **RDS** para consulta posterior.

### ⚖️ Licença

O conteúdo é licenciado sob a **[Licença MIT](LICENSE)**.

---
<div align="center">

## **✨ 🧑‍💻 Autora ✨**

| Integrante                  |                                                      GitHub                                                      |                                                                  LinkedIn                                                                  |                                                             Instagram                                                             |
| :-------------------------- | :--------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------: |
| **Talita Mendonça Marques** | [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github)](https://github.com/skyzinha-chan) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/talita-mendonca-marques/) | [![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram)](https://www.instagram.com/skyzinha_chan/) |

</div>



<div align="center">

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/skyzinha-chan">
        <img src="./assets/talita-mendonca.jpg" width="150px;" alt="Foto de Talita Mendonça Marques" style="border-radius:50%;"/>
        <br />
        <sub><b>Talita Mendonça Marques</b></sub>
      </a>
    </td>
    
  </tr>
</table>

**Licenciatura em Ciência da Computação**
<br>
Instituto Federal de Educação, Ciência e Tecnologia de Mato Grosso do Sul - **Campus Jardim**

</div>
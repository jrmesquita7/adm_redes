---

## **Título da Aula: Automatizando Tarefas em Redes com Scripts**  

---

### **Objetivo Geral**  
Capacitar os alunos a criar scripts simples em Bash, Python e VBScript para automatizar tarefas comuns na administração de redes.

---

### **Objetivos Específicos**
1. Compreender a importância da automação na administração de redes.  
2. Conhecer as linguagens Bash, Python e VBScript e suas aplicações.  
3. Criar scripts básicos para tarefas práticas.  

---

### **Público-Alvo**  
Estudantes ou profissionais iniciantes em redes e programação.

---

## **Plano de Aula**

---

#### **1.1. O que é Administração de Redes?**
- Monitoramento e gerenciamento de dispositivos, serviços e usuários.  
- Exemplos de tarefas: verificar conectividade, coletar logs, configurar dispositivos.  

#### **1.2. Por que automatizar?**
- **Vantagens:**  
  - Reduz erros humanos.  
  - Economiza tempo.  
  - Facilita tarefas repetitivas.  
- Exemplos de automação em redes:  
  - Scripts para backup automático de configurações de roteadores.  
  - Verificação de conectividade entre dispositivos.

#### **1.3. Linguagens abordadas:**
1. **Bash:** Ideal para Linux/Unix, interação com comandos do sistema.  
2. **Python:** Versátil, com bibliotecas para redes e sistemas multiplataforma.  
3. **VBScript:** Integrado ao Windows, útil para automação em ambientes corporativos.

---

### **2. Fundamentos das Linguagens**

#### **2.1. Bash Script**
- Sintaxe básica: comandos, variáveis e laços.  
- Exemplo:  
  ```bash
  echo "Digite um nome:"
  read nome
  echo "Olá, $nome!"
  ```

#### **2.2. Python**
- Sintaxe básica: funções, manipulação de strings e bibliotecas.  
- Exemplo:  
  ```python
  nome = input("Digite um nome: ")
  print(f"Olá, {nome}!")
  ```

#### **2.3. VBScript**
- Sintaxe básica: variáveis e interação com o Windows.  
- Exemplo:  
  ```vbscript
  nome = InputBox("Digite um nome")
  MsgBox "Olá, " & nome
  ```

---

### **3. Aplicações Práticas**

#### **3.1. Bash Script: Verificar conectividade**
- Script:  
  ```bash
  echo "Digite o IP:"
  read IP
  ping -c 1 $IP &>/dev/null && echo "Host $IP está ativo" || echo "Host $IP está inativo"
  ```

#### **3.2. Python: Obter informações de rede**
- Script:  
  ```python
  import socket
  hostname = socket.gethostname()
  ip_address = socket.gethostbyname(hostname)
  print(f"Nome do host: {hostname}")
  print(f"Endereço IP: {ip_address}")
  ```

#### **3.3. VBScript: Exibir IP no Windows**
- Script:  
  ```vbscript
  Set objWMIService = GetObject("winmgmts:\\.\root\cimv2")
  Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")
  For Each objItem in colItems
      WScript.Echo "Endereço IP: " & Join(objItem.IPAddress, ", ")
  Next
  ```

---

### **4. Atividade Prática**

#### **4.1. Proposta:**  
Os alunos devem criar scripts simples para resolver os seguintes problemas:  
1. Verificar se vários IPs estão ativos na rede.  
2. Coletar informações de rede (nome do host e endereço IP).  
3. Registrar os resultados em um arquivo de log.

#### **4.2. Etapas:**
1. Dividir a turma em três grupos (um para cada linguagem).  
2. Cada grupo cria um script baseado no problema designado.  
3. Os alunos apresentam os scripts criados e os resultados obtidos.  

---

---

## **Materiais de Apoio**

1. **Slides com conteúdo teórico** (introdução e fundamentos).  
2. **Ambiente de teste configurado**:  
   - Máquina Linux ou Windows para rodar os scripts.  
   - Editor de texto (ex.: VS Code).  
3. **Documentação básica:**  
   - Introdução ao Bash: [GNU Bash Manual](https://www.gnu.org/software/bash/manual/bash.html)  
   - Python Networking: [Python Socket](https://docs.python.org/3/library/socket.html)  
   - VBScript: [Microsoft VBScript Reference](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/legacy/dnangelb(v=vs.85))

---

Se precisar dos **slides prontos ou um PDF do material**, posso gerar também! 😊

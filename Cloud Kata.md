# Cloud Katas

## DevOps Katas: effettuare il deploy automatico di una applicazione web su una infrastruttura cloud.

- Ambiente di sviluppo: Java, framework spring
- Sistema di versionamento del codice: Git
- Piattaforma per il versionamento del codice: Github www.github.com
- Piattaforma di Continous Integration/Continous Deployment: Travis www.travis-ci.com
- Infrastruttura cloud: dockerhub www.dockerhub.com + heroku www.heroku.com

**Precondizioni**: linux debian/ubuntu, JDK >8 maven >3  e Git  installati sulla macchina;  account personali per github, travis-ci, heroku,dockerhub 

### **Kata #1 Commit: metti il tuo lavoro al sicuro**

Sei un Developer, e vuoi creare la tua web application, il tuo linguaggio di riferimento è Java e con spring e spring-boot puoi rapidamente ottenere un microservizio. La prima cosa che fai è assicurarti che il codice sia "versionato" , ovvero che sia memorizzato su un server centrale e che sia accessibile da te e dai tuoi collaboratori. 

- crea un nuovo repository su Github 

  - vai su https://github.com/new ed inserisci il nome del tuo progetto:  devOpsKata1  per semplicità  scegli "public" e **non** selezionare altre opzioni (licenza ed readme)

- crea una directory che contenga il tuo progetto

  - `mkdir devOpsKata1`

- vai nella directory

  - `cd devOpsKata1`

- Inizializza il progetto affinchè vengano tracciate le modifiche e prendi confidenza con il ciclo di "push->commit" per salvare il tuo lavoro sul  repository remoto di git :

  ```
  #crea un file (anche vuoto) di nome README.md 
  git init
  git add README.md
  #Commit: salva il tuo lavoro sulla copia locale del tuo repository
  git commit -m "project init"
  #aggiungi la url del tuo repository remoto
  git remote add origin https://github.com/${username Github}/devOpsKata1.git
  #salva la tua commit sul server remoto
  git push -u origin master
  ```


Altri kata: aggiungere un nuovo file al repository cancellarlo e verificare la storia 

### Kata #2 DRY Scrivi la tua (mini) applicazione

**Don't Repeat Yourself**. Negli anni le diverse community opensource hanno identificato dei meccanismi stabili per consentire agli sviluppatori di iniziare un nuovo progetto non proprio da zero
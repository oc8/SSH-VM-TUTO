<div id="top"></div>

<div align="center">
  <h3 align="center">SSH-VM-TUTO</h3>

  <p align="center">
    Connexion d'un terminal et de VS code en SSH a une VM   <br />
    Parfait pour inception
    <br />    <br />    <br />
  </p>
</div>

## Paramétrer votre VM
<img width="883" alt="portssh" src="https://user-images.githubusercontent.com/46847941/150156747-ccfd58ab-b8d9-45ab-af08-ed90ac329026.png">


## Dans le terminal de la VM    <br />
* 
  ```
  sudo usermod -aG sudo {loginVM}
<br />

* 
  ```
  sudo apt-get install openssh-server
<br />

* 
  ```
  sudo apt-get install ssh
<br />

## Connecter un terminal    <br />
* 
  ```
  ssh -p 3022 {loginVM}@127.0.0.1
<br />

## Connecter VS code    <br />
* Installer l'extension: Remote - SSH    <br />
* Ajouter une nouvelle connexion SSH    <br />
* Connecter vous avec ces identifiants    <br />
-> ssh -p 3022 {loginVM}@127.0.0.1    <br />
-> mdp de votre VM    <br />
<img width="252" alt="Screen Shot 2022-01-19 at 4 05 52 PM" src="https://user-images.githubusercontent.com/46847941/150157638-11b84507-16a9-43c2-aa1c-4a641d10ed30.png">
 
<br />
 
* Si vous ne possedez pas les droits de modification    <br />
  
    ```
    sudo chmod -R 755 .
 <br />
 
* Erreur: kex_exchange_identification: Connection closed by remote host    <br />
  
  ```
  sudo service ssh start
 <br />

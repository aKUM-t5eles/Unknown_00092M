# Instalando o Terraform

O pacote vem da página de downloads do fabricante, onde cada sistema operacional tem seu instalador. Basta escolher a plataforma e baixar.




---

# Instalando o Jenkins

O repositório de pacotes da distribuição serve para instalar e atualizar a ferramenta. Primeiro, adicione a chave de assinatura do repositório:

```
wget -qO- <endereço da chave do repositório> | sudo gpg --dearmor -o <arquivo de chaves do sistema>
```

Depois acrescente o repositório à lista do gerenciador de pacotes:

```
  echo "deb [signed-by=<arquivo de chaves>] <endereço do repositório> binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list
```

Atualize o índice local e instale, primeiro as fontes e o runtime Java, depois o próprio Jenkins:

```
  sudo apt-get update
  sudo apt-get install -y fontconfig openjdk-17-jre
  sudo apt-get install -y jenkins
```


A documentação oficial do repositório tem o mesmo passo a passo.



# Usando o Terraform

Basta chamar o binário no terminal.



# Usando o Jenkins

Inicie o serviço:

```
sudo service jenkins start
```

Depois abra a interface web no endereço padrão da máquina local.

A senha inicial está num arquivo dentro da instalação; a imagem do projeto mostra o caminho exato: `/var/lib/jenkins/secrets/initialAdminPassword`.

# Chave na nuvem

Obviamente removi a chave da conta de nuvem logo em seguida. Em versões futuras do script a ideia é ler tudo de variáveis de ambiente.
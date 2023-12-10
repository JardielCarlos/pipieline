# Execução do Projeto `Pipeline` com Jenkins
## Permissões Necessárias:
Entre no diretório abaixo
```
  cd /var/run
```
De as permissões ao docker.sock
```
  sudo chmod 777 docker.sock
```
Adicionar um novo usuário chamado `jenkins`.
```
  useradd jenkins
```
Adiciona o usuário `jenkins` ao grupo `docker`. Isso permite que o usuário `jenkins` execute comandos Docker sem precisar de `sudo`.
```
  sudo usermod -aG docker jenkins
```
 Esse comando é usado para verificar se o usuário `jenkins` foi adicionado ao grupo `docker`.
```
  grep docker /etc/group
```
# Criando a Pipeline
Faça login no Jenkins

e faça os seguintes passos:

1. Clique em: `+ Novo Tarefa`
2. Escreva o nome da pipeline
3. Selecione nas opções disponíveis: `pipeline` e depois clique em `Tudo certo`
4. Escreva uma descrição (Opcional)
5. Desça até a seção `Pipeline`
6. Em `definition` onde tem escrito `Pipeline script` clique nele e selecione `Pipeline script from SCM`
7. Na seção `SCM` clique nele e selecione `git`
8. Aparecerá agora `Repository URL` onde você vai colocar a url desse projeto que é `https://github.com/JardielCarlos/pipieline.git` 
9. Mais embaixo aparecerá `Branch Specifier` onde deve ter o nome da branch que no caso desse projeto é `*/main`
10. Por ultimo clique em `Salvar` para finalizar a configuração da pipeline

# Executando a pipeline criada

* Após criar a pipeline no lado direito deve aparecer uma opção chamada `Construir agora` clique nele e após isso clique em `Open Blue Ocean` local no qual pode gerenciar a sua pipeline com uma interface gráfica mais agradável.

## Desafio 1 (B)
Para extrair `challenges.tar.gz`, usei o comando:

tar -xzvf challenges.tar.gz

## Desafio 2 (B)
Para entrar no diretório `challenges/`, utilizei o comando:
cd challenges


## Desafio 3 (B)
Para listar o conteúdo do diretório `challenges`, usei:

ls challenges/

## Desafio 4 (B)
Para criar o diretório `foo` dentro de `challenges`, usei:

mkdir challenges/foo

## Desafio 5 (I)
Para criar todas as subpastas `foo/bar/1/2/3` dentro de `challenges`, usei:
mkdir -p challenges/foo/barr/1/2/3


##Desafio 6 (B)
Para remover o diretório foo e todo o seu conteúdo, utilizei o comando:

rm -rf challenges/foo

##Desafio 7 (B)
Para imprimir o texto "Olá, Mundo", usei o comando:
echo "Olá, Mundo"

##Desafio 8 (B)
Para criar um arquivo chamado hello.txt contendo o texto "Hello World", usei:

echo "Hello World" > hello.txt

##Desafio 9 (B)
Para criar um arquivo vazio chamado empty.txt, usei:
touch empty.txt

##Desafio 10 (B)
Para remover o arquivo empty.txt, usei:
rm empty.txt

##Desafio 11 (I)
Uma segunda maneira de criar um arquivo vazio chamado empty.txt foi:

echo -n > empty.txt

##Desafio 12 (I)
> empty.txt

##Desafio 13 (B)
Para copiar o arquivo hello.txt e nomear a cópia como goodbye.txt, usei:
cp hello.txt goodbye.txt

##Desafio 14 (B)
Para renomear goodbye.txt para hello_copy.txt, usei:
mv goodbye.txt hello_copy.txt

##Desafio 15 (I)
Para provar que o conteúdo de hello.txt e hello_copy.txt são idênticos, usei:
diff hello.txt hello_copy.txt
Se o comando não retornar nada, os arquivos são idênticos.

##Desafio 16 (B)
Para concatenar o conteúdo de hello.txt e hello_copy.txt em um novo arquivo chamado 2_hellos.txt, usei:

cat hello.txt hello_copy.txt > 2_hellos.txt



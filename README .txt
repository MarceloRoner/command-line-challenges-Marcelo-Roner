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


##Desafio 17 (B)
Para obter o caminho completo do meu diretório de trabalho atual, usei o comando:

pwd


##Desafio 18 (B)

Para listar o conteúdo do diretório desafios e mostrar as permissões para cada arquivo, usei:
ls -l desafios/

Desafio 19 (B)
Para acrescentar texto ao final de restricted.txt, usei os seguintes comandos em duas etapas:

echo "Texto adicional" >> restricted.txt

##Desafio 20 (B)
Para executar o programa hello_executable, utilizei:

./hello_executable

##Desafio 21 (B)
Para executar o programa challenge_20, usei dois passos:

chmod +x challenge_20  # Torna o arquivo executável, caso necessário
./challenge_20

##Desafio 22 (B)
Para compilar e executar compile_me.c, segui estas etapas:

gcc compile_me.c -o compile_me
./compile_me

##Desafio 23 (A)
Para executar o programa redirect e coletar sua saída em output.txt, usei:

./redirect > output.txt

##Desafio 24 (B)
Para obter a data e a hora atuais, utilizei:
date

##Desafio 25 (B)
Para mostrar todos os processos em execução no meu computador, usei:
ps aux

##Desafio 26 (B)
Para exibir o número de processadores/núcleos disponíveis, utilizei:

nproc

Ou, alternativamente:
cat /proc/cpuinfo | grep -c processor

##Desafio 27 (B)
Para descobrir a versão do kernel Linux em execução, utilizei:
uname -r

## Desafio 28 (B)
Para encontrar o arquivo dentro do diretório `bunch_of_files/` que contém a string `"Você encontrou a agulha no palheiro!"`, usei o seguinte comando:
grep -Rl "Você encontrou a agulha no palheiro!" bunch_of_files/

Desafio 29 (B)
Para imprimir as primeiras 25 linhas do arquivo people.csv, utilizei:
head -n 25 people.csv
Desafio 30 (B)
Para imprimir as últimas 25 linhas do arquivo people.csv, utilizei:

tail -n 25 people.csv
Desafio 31 (I)
Para exibir apenas as diferenças entre os arquivos greeting1.txt e greeting2.txt, utilizei:

diff greeting1.txt greeting2.txt
Desafio 32 (I)
Para imprimir "Olá", aguardar 5 segundos e depois imprimir "mundo!", utilizei:
echo "Olá" && sleep 5 && echo "mundo!"

Desafio 33 (I)
Para criar um arquivo de 1 MB cheio de zeros, utilizei:
Desafio 34 (I)
Para criar um arquivo de 2 MB cheio de dados aleatórios, utilizei:
dd if=/dev/urandom of=arquivo2mb.bin bs=1M count=2
Desafio 35 (I)
Para contar o número de linhas no arquivo README.txt, utilizei:
wc -l README.txt
Desafio 36 (B)
Para exibir o conteúdo do README.txt ao contrário (última linha primeiro), utilizei:

tac README.txt
Desafio 37 (I)
Para exibir todos os sobrenomes contidos no arquivo people.csv, utilizei:

cut -d ',' -f 2 people.csv
Desafio 38 (A)
Para contar o número de sobrenomes exclusivos no arquivo people.csv, utilizei:
cut -d ',' -f 2 people.csv | sort | uniq | wc -l

Desafio 39 (A)
Você acidentalmente contou o cabeçalho CSV no desafio anterior? Para corrigir isso, utilizei:


tail -n +2 people.csv | cut -d ',' -f 2 | sort | uniq | wc -l
Explicação:

tail -n +2: Ignora a primeira linha (cabeçalho) do arquivo CSV.
O restante do comando é igual ao Desafio 38.
Desafio 40 (A)
Há uma segunda maneira de excluir o cabeçalho CSV da sua contagem. Encontrei-a usando:


cut -d ',' -f 2 people.csv | tail -n +2 | sort | uniq | wc -l
Explicação:

tail -n +2: Remove a primeira linha após extrair os sobrenomes.
Desafio 41 (A)
Para provar se um método é mais eficiente (mais rápido) que o outro, usei o comando time para medir o tempo de execução de cada abordagem:


time tail -n +2 people.csv | cut -d ',' -f 2 | sort | uniq | wc -l
time cut -d ',' -f 2 people.csv | tail -n +2 | sort | uniq | wc -l
O comando time exibe o tempo real, do usuário e do sistema para cada execução.

Desafio 42 (A)
Para contar o número de pessoas com o primeiro nome "Josias" em people.csv, utilizei:


grep -i '^Josias,' people.csv | wc -l
Explicação:

grep -i '^Josias,': Procura por linhas que começam com "Josias" (ignorando maiúsculas/minúsculas).
wc -l: Conta o número de linhas correspondentes.
Desafio 43 (I)
Para contar o número de arquivos (não diretórios) no diretório challenges, utilizei:


find challenges/ -type f | wc -l
Explicação:

find challenges/ -type f: Encontra todos os arquivos no diretório challenges.
wc -l: Conta o número de resultados.
Desafio 44 (I)
Para contar o número de subdiretórios no diretório desafios, utilizei:

find desafios/ -type d | wc -l
Explicação:

find desafios/ -type d: Encontra todos os diretórios no diretório desafios.
wc -l: Conta o número de resultados.
Desafio 45 (I)
Para remover todos os arquivos com "deleteme" no nome, utilizei:

find . -name "*deleteme*" -exec rm {} \;
Explicação:

find . -name "*deleteme*": Localiza todos os arquivos com "deleteme" no nome.
-exec rm {} \;: Remove cada arquivo encontrado.
Desafio 46 (I)
No Desafio 28, encontrei o arquivo que continha a string "Você encontrou a agulha no palheiro!". Para substituir essa string por "A agulha foi removida.", utilizei:


sed -i 's/Você encontrou a agulha no palheiro!/A agulha foi removida./g' $(grep -Rl "Você encontrou a agulha no palheiro!" bunch_of_files/)
Explicação:

grep -Rl: Encontra o arquivo contendo a string.
sed -i: Substitui a string no arquivo encontrado.
Desafio 47 (A)
Para transformar people.csv de delimitado por , para delimitado por | e salvar o resultado em people_pipe.csv, utilizei:


awk -F',' '{OFS="|"; print $1, $2, $3}' people.csv > people_pipe.csv
Explicação:

-F',': Define a vírgula como delimitador de entrada.
OFS="|": Define o caractere | como delimitador de saída.
print $1, $2, $3: Imprime as colunas separadas por |.
Desafio 48 (A)
Para encontrar todos os arquivos em bunch_of_files/ que são duplicados de file001.rand, utilizei:

md5sum bunch_of_files/file001.rand | awk '{print $1}' > checksum.txt
find bunch_of_files/ -type f -exec md5sum {} \; | grep -f checksum.txt
Explicação:

md5sum: Calcula o hash MD5 do arquivo.
find e grep: Comparam o hash de outros arquivos com o hash de file001.rand.
Desafio 49 (A)
Executei este desafio em exatamente 2 passos:

Criar um arquivo vazio chamado supercalifragilisticexpialidocious.txt:

touch supercalifragilisticexpialidocious.txt
Remover o arquivo criado, usando no máximo 5 caracteres:

rm s*
Desafio 50 (A)
Para criar um conjunto de arquivos vazios com nomes no formato LN.txt (onde L é uma letra e N é um número), utilizei:


touch {a,b,c}{1,2,3}.txt
Explicação:

{a,b,c}: Gera as letras a, b e c.
{1,2,3}: Gera os números 1, 2 e 3.
Combinações geram 9 arquivos: a1.txt, a2.txt, ..., c3.txt.


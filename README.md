# -Reconhecimento-Facial-e-transforma-o-de-imagens-em-Dados-no-Azure-MLROTEIRO PARA DOCUMENTAÇÃO E PUBLICAÇÃO DE UM PROJETO NO GITHUB

1. Crie um novo repositório no GitHub


Acesse github.com e faça login na sua conta.

Clique em "New repository" (Novo repositório).

Escolha um nome significativo para o projeto (exemplo: reconhecimento-texto-imagens).

Adicione uma breve descrição.

Marque a opção para adicionar um README se preferir.

Clique em "Create repository".

2. Estruture as pastas do projeto no seu computador


Clone o repositório recém-criado para o seu computador com:
git clone https://github.com/seuusuario/nomedorepositorio.git


Navegue até a pasta do projeto no seu computador.

Crie uma pasta chamada inputs para armazenar todas as imagens utilizadas no projeto.

Crie uma pasta chamada output para salvar os resultados do reconhecimento de texto (pode ser em formato .txt, .csv, .json, etc.).

3. Adicione os arquivos de entrada e saída


Salve todas as imagens originais que você utilizou na pasta inputs.

Salve os arquivos resultantes do reconhecimento de texto na pasta output.

Certifique-se de nomear os arquivos de maneira organizada, relacionando as imagens com seus respectivos resultados.

4. Crie e escreva o arquivo README.md


No diretório principal do projeto, crie (ou edite) o arquivo README.md.


Inclua informações como:



Visão geral do projeto.

Etapas seguidas para processar as imagens.

Prints de tela do processo (salve as imagens dos prints na pasta inputs e adicione referências a elas no README).

Principais aprendizados, insights e desafios enfrentados.

Possibilidades de aplicação do conhecimento adquirido em outros contextos.


Exemplo de estrutura do README.md:


# Reconhecimento de Texto em Imagens

## Sobre

Projeto para extrair texto de imagens utilizando [nome da ferramenta/método].

## Estrutura do Projeto

- inputs/: imagens originais utilizadas
- output/: arquivos com o texto extraído de cada imagem

## Processo

1. Coleta das imagens
2. Processamento com [nome do software ou biblioteca]
3. Armazenamento dos resultados
4. Análise dos textos extraídos

![Exemplo de imagem processada](inputs/exemplo.png)

## Aprendizados

- Compreensão do workflow de OCR
- Importância do pré-processamento das imagens
- Possíveis melhorias para projetos futuros

## Possibilidades de Uso

- Digitalização de documentos
- Análise de recibos e notas fiscais
- Extração de dados para automação


5. Suba todas as alterações para o GitHub


Use o seguinte comando para adicionar e fazer o commit dos arquivos:
git add .
git commit -m "Estrutura inicial do portfólio e documentação do projeto"
git push origin main


6. Compartilhe o link do repositório


Acesse seu projeto no GitHub, copie o link na barra de endereço e compartilhe com quem desejar.


No ambiente da plataforma, envie o link pelo botão “entregar projeto”.

Siga esse roteiro sempre que concluir um projeto. Isso demonstra não só seu conhecimento técnico, mas também sua habilidade de organizar, documentar e apresentar o resultado do seu trabalho de forma profissional.
etectar faces no Vision Studio

Soluções de visão computacional frequentemente precisam de IA capaz de detectar rostos humanos. Suponha que a empresa fictícia Northwind Traders queira saber onde seus clientes estão em uma loja para melhor atendê-los. Uma maneira de fazer isso é verificando se há rostos nas imagens e, em caso positivo, obter as coordenadas dos retângulos que mostram suas localizações.

1. Criar um recurso do Azure AI Services
Você pode usar o serviço Azure AI Face com um recurso multi-serviço do Azure AI. Caso ainda não tenha, crie um recurso Azure AI Services na sua assinatura Azure.


Em outra aba do navegador, acesse o portal Azure em https://portal.azure.com e faça login com a conta Microsoft vinculada à sua assinatura Azure.

Clique em + Criar um recurso e pesquise por "Azure AI services". Selecione para criar um plano do Azure AI services.

Na página de criação:

Assinatura: Sua assinatura Azure

Grupo de recursos: Selecione ou crie um grupo de recursos com um nome único

Região: Escolha a região geográfica mais próxima (ex: "East US 2" se estiver no leste dos EUA)

Nome: Escolha um nome único

Plano de preços: Standard S0

Termos de uso: Marque a caixa confirmando que leu e entendeu os termos
![Captura de tela de 2025-06-17 18-50-04](https://github.com/user-attachments/assets/4194f21b-ff05-4183-9278-3b3bbdeb5086)

Clique em Revisar + criar e depois Criar. Aguarde a implantação ser concluída.
![Captura de tela de 2025-06-17 18-50-23](https://github.com/user-attachments/assets/ca51b650-026a-474a-996e-24419368ef35)

3. Detectar faces com o Vision Studio

Abra o Vision Studio: https://portal.vision.cognitive.azure.com

Na página inicial, selecione a aba Face e depois o bloco Detect Faces in an image.

Em "Try It Out", leia e reconheça a política de uso de recursos, marcando a caixa.

Selecione cada uma das imagens de exemplo e observe os dados de detecção de faces retornados.

Testando com suas próprias imagens:

Baixe exemplos de imagens em https://aka.ms/mslearn-detect-faces (arquivo detect-faces.zip) e extraia em seu computador.

Encontre o arquivo store-camera-1.jpg, faça upload e analise os detalhes de detecção de face.

Repita com store-camera-2.jpg e store-camera-3.jpg.

Observe, por exemplo, que no arquivo store-camera-3.jpg a Azure AI Face não detecta um rosto que está obstruído.


Se desejar, experimente outras imagens fornecidas ou use suas próprias imagens para testar o reconhecimento.

4. Limpeza
Depois que terminar, se não for mais usar o serviço, exclua os recursos criados para evitar cobranças:


No portal Azure (https://portal.azure.com), acesse o grupo de recursos do serviço criado.

Selecione o recurso, clique em Excluir e confirme em Sim.

O recurso será removido.
![Captura de tela de 2025-06-17 18-50-40](https://github.com/user-attachments/assets/308a9327-8f4e-4182-a050-a1a83ad791fa)




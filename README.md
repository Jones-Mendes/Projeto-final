# Projeto Final de Realidade Aumentada - iRede

## Sobre o Projeto
Este projeto foi desenvolvido como **Projeto Final do Curso de Realidade Aumentada (RA)** oferecido pelo **iRede**.

A formação foi ministrada pelo **Professor Alysson Diniz**, com acompanhamento dos monitores **Maisa Lourenco** e **Rister Saulo**.
Autor: **Jones de Oliveira Mendes**

A proposta segue e aprofunda o conceito da atividade anterior: a representacao de predios e personalidades historicas do Ceara. Nesta versao final, o foco e o **escritor Jose de Alencar**.

## Objetivo
Criar uma experiencia de RA interativa e educativa, combinando:
- visualizacao 3D de elementos historicos;
- interacao por gestos em dispositivos moveis;
- animacoes em tempo real;
- narrativa em audio para enriquecer a experiencia do usuario.

## Conceito da Experiencia
A aplicacao utiliza marcadores AR para apresentar dois modelos 3D na cena:
- `ZeAlencar.glb` (referencia a Jose de Alencar);
- `livro.glb` (elemento simbolico ligado a producao literaria).

Quando os marcadores sao reconhecidos, os elementos aparecem no ambiente fisico e podem ser manipulados diretamente pelo usuario por toque.

## Funcionalidades Principais
### 1. Reconhecimento por Marcadores (AR.js + A-Frame)
- leitura de marcadores `hiro` e `kanji`;
- ancoragem de modelos 3D na cena aumentada;
- renderizacao em tempo real via camera do dispositivo.

### 2. Interacoes por Toque (6 DoF orientado a uso pratico)
- selecao do objeto tocado com **Raycaster**;
- gesto de 1 dedo para rotacao;
- gesto de 2 dedos para translacao no plano da tela;
- pinca para escala (zoom);
- rotacao adicional por torcao de dois dedos.

### 3. Logica de Proximidade entre Marcadores
- calculo de distancia em coordenadas de mundo entre `hiro` e `kanji`;
- ativacao de comportamentos conforme estado de proximidade;
- controle de transicoes para evitar saltos visuais.

### 4. Animacoes
- **Spin** continuo do livro em situacao de proximidade;
- **Flutuacao** suave quando apenas o marcador do livro esta visivel.

### 5. Narrativa em Audio
- botao fixo para reproduzir/parar a historia;
- alternancia dinamica de rotulo entre ouvir e parar;
- reset do audio para garantir repeticao consistente.

## Estrutura do Projeto
- `index.htm`: estrutura principal da cena AR, componentes e logica JavaScript;
- `styles.css`: estilos de interface, incluindo o botao de audio;
- `ZeAlencar.glb`: modelo 3D relacionado a Jose de Alencar;
- `livro.glb`: modelo 3D de apoio narrativo;
- `explicando.mp3`: trilha de narracao da experiencia.

## Tecnologias Utilizadas
- **A-Frame** para construcao da cena 3D;
- **AR.js** para rastreamento de marcadores em navegador;
- **Three.js** (via A-Frame) para Raycaster e vetores;
- **HTML, CSS e JavaScript** para interface e regras de interacao.

## Requisitos para Execucao
- dispositivo com camera (preferencialmente smartphone);
- navegador moderno com suporte a WebRTC e WebGL;
- permissao de acesso a camera;
- ambiente servido por HTTPS.

## Como Executar
1. Abra a pasta do projeto em um servidor local (ex.: Live Server no VS Code).
2. Acesse a pagina no navegador do celular ou computador com camera.
3. Permita acesso a camera quando solicitado.
4. Posicione os marcadores `hiro` e `kanji` para visualizar os modelos.
5. Interaja com toques para mover, rotacionar e escalar os objetos.
6. Use o botao de audio para ouvir ou parar a narrativa.

## Resultado Pedagogico
Este trabalho demonstra a aplicacao integrada dos conceitos do curso:
- modelagem de experiencia imersiva;
- interacao humano-computador em RA;
- narrativa digital aplicada ao patrimonio historico-cultural do Ceara;
- implementacao tecnica funcional com foco em usabilidade.

## Creditos
**Projeto Final do Curso de RA - iRede**  
Professor: **Alysson Diniz**  
Monitores: **Maisa Lourenco** e **Rister Saulo**
Aluno: **Jones de Oliveira Mendes**

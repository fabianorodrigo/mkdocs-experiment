# Introdução

O decreto 8936/2016, instituiu a Plataforma de Cidadania Digital e dispôs sobre a oferta dos serviços públicos digitais, no âmbito dos órgãos e das entidades da administração pública federal direta, autárquica e fundacional.

No seu artigo 3º, incisos IV e V foi instituído a ferramenta de avaliação da satisfação dos usuários em relação aos serviços públicos prestados e o painel de monitoramento do desempenho dos serviços públicos prestados.

Entre as informações mínimas que deverão estar disponíveis no painel para cada serviço, órgão ou entidade da administração pública federal, estão o volume de solicitações, tempo médio de atendimento e o nível de satisfação dos usuários.

# Fluxo do Cidadão - Da solicitação à avaliação do serviço

## Solicitação do serviço

Para solicitar um determinado serviço público digital, o cidadão poderá fazê-lo tanto através da página deste serviço no portal Gov.br quanto poderá acessá-lo navegando diretamente no sistema de informação do órgão que presta o serviço. Por exemplo, para utilizar o serviço de Emissão de Comprovante de Situação Cadastral no CPF, prestado pela Receita Federal, o cidadão poderá acessar diretamente o endereço https://servicos.receita.fazenda.gov.br/servicos/cpf/consultasituacao/ConsultaPublica.asp ou acessar <gente, cadê a página do serviço???>

## Registro do acompanhamento do serviço/etapa

Quando o sistema de informação do órgão recebe a solicitação do serviço pelo cidadão, ele deve registrar essa solicitação via API de Acompanhamento de Serviços. Desta forma, tanto o cidadão poderá acompanhar todas as suas solicitações de serviços públicos de forma unificada (em breve no portal Gov.br) quanto o gestor do serviço poderá usufruir de mentoria e ferramentas de gestão elaboradas pela Secretaria de Governo Digital para o acompanhamento e o aperfeiçoamento dos serviços prestados pelo seu órgão.

Chamamos o registro dessa solicitação de ACOMPANHAMENTO. Como veremos mais adiante neste Manual, entre outras informações, um Acompanhamento vai ter o número do protocolo, que identifica aquela solicitação do cidadão de forma única dentro do órgão.

> **_ATENÇÃO:_** Por ora, nosso único objetivo é compreender o fluxo de interações entre o cidadão, o órgão prestador do serviço digital e a API de Avaliação e Acompanhamento da Secretaria de Governo Digital. Mais à frente, será explicado detalhadamente como realizar a integração entre os sistemas de informação do órgão e a API da SGD.

Muitos serviços públicos são prestados em etapas, eventualmente, passando por diferentes secretarias/coordenações dentro do órgão que darão diferentes contribuições para atender por completo a solicitação do cidadão. Idealmente, o órgão poderá registrar um ACOMPANHAMENTO para cada uma das diferentes etapas da prestação do serviço. Assim, consequentemente, terá acesso a informações mais detalhadas sobre a prestação do serviço, possibilitando melhorias pontuais para melhorar a experiência do cidadão.

## Conclusão do serviço/etapa

Após a conclusão de cada uma das etapas do serviço ou do serviço como um todo, o sistema de informação do órgão fará uma nova interação com a API de Avaliação e Acompanhamento. Desta vez, para informar a conclusão de uma etapa/serviço e, assim, obter um link único para o um formulário de avaliação para o qual o cidadão será direcionado.

## Avaliação do serviço/etapa

Quando o cidadão é direcionado para este link, ele visualizará a tela que pode ser vista na imagem a seguir. Nela, o cidadão poderá avaliar a etapa do serviço que acabou de ser concluída ou, caso seja prestado em uma etapa única, avaliar o serviço como um todo. O cidadão deverá escolher entre 1 e 5 estrelas para manifestar seu nível de satisfação. Em seguida, poderá escolher até 3 critérios que motivaram sua avaliação.

Importante lembrar que a escolha dos critérios é opcional, assim, o usuário pode concluir sua avaliação sem selecionar nenhum critério.

Também de forma opcional, o cidadão poderá preencher textualmente comentários, elogios ou críticas sobre a sua experiência com o serviço.

![Formulário de Avaliação do Serviço](./img/form_avaliacao_2.png 'Formulário de Avaliação do Serviço')

Ao clicar no botão "Enviar Avaliação", a sua nota, critérios e comentários seráo devidamente registrados e ele será encaminhado para uma página de confirmação do registro da sua avaliação de satisfação.

![Página de confirmação da Avaliação do Serviço](./img/form_avaliacao_3.png 'Página de confirmação da Avaliação do Serviço')

# Integração com a API de Avaliação e Acompanhamento

Entendido o propósito, a jornada do cidadão pela prestação de serviços digitais até a avaliação do seu nível de satisfação, e os ganhos que tanto a sociedade brasileira quanto os próprios gestores dos serviços poderão colher com essa iniciativa da Secretaria de Governo Digital, o próximo passo é detalharmos como operacionalizar essa ferramenta para cada um dos serviços digitais do seu órgão.

Faremos isso em etapas que estão listadas a seguir:

[Fluxo de interação](1.fluxo_cidadao.md)

[Credenciais](1.fluxo_cidadao.md)

[xpto](1.fluxo_cidadao.md)

## Commands

- `mkdocs new [dir-name]` - Create a new project.
- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build the documentation site.
- `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

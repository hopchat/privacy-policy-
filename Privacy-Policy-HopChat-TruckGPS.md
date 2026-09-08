Politica de privacidade
1. Responsável e contato
O Truck GPS é desenvolvido por alpgameplays. Contato: https://github.com/alpgameplays.

2. O que o aplicativo faz
A primeira versão atende ao American Truck Simulator (ATS). O celular recebe telemetria do computador pela rede local. O cálculo e o recálculo de rotas usam um servidor na internet, tanto no plano gratuito quanto no PRO.

3. Dados no celular e na rede local
O aplicativo guarda preferências, aceite dos termos, identidade do aparelho, credencial de pareamento e documentos de direito de uso. A câmera é usada para ler o QR code de pareamento; é possível parear digitando os dados. A imagem do QR não é gravada nem enviada ao servidor de rotas. A posição exibida é a do caminhão no jogo, não a localização GPS do celular.

4. Dados enviados ao servidor
Para abrir a sessão e controlar acesso e cota, a API recebe um identificador do aparelho, plataforma, versão do aplicativo e informações dos DLCs. Para calcular rotas, recebe jogo, posição e direção do caminhão no mundo virtual, destino e informações necessárias ao pedido. A API registra consumo de quilômetros e eventos de conta e cobrança. A comunicação também expõe o endereço IP ao serviço, usado no controle de requisições.

O servidor guarda usuários, aparelhos vinculados, compras, direitos de uso, histórico de cobrança de rotas e registros de auditoria. Esses dados permitem prestar o serviço, conferir assinaturas, controlar cota e investigar falhas.

5. Login e compras
O login Google usa Firebase Authentication. O provedor processa a autenticação; o app recebe informações da conta para exibição e um token que a API verifica para vincular o aparelho ao identificador da conta. O aplicativo não pede sua senha Google diretamente.

Compras e assinaturas usam Google Play e RevenueCat. Identificadores de compra, produto, situação e períodos da assinatura são usados para conferir o direito PRO. A API recebe comprovantes e atualizações de cobrança. O Truck GPS não recebe o número completo do seu cartão. As compras seguem também os termos e políticas desses provedores.

6. Terceiros e publicidade
O app utiliza Unity, Firebase Authentication, Google Play, RevenueCat e Google AdMob.

Na versão gratuita, um banner é exibido no rodapé da tela do mapa. Ele é servido pelo Google AdMob, que pode usar o identificador de publicidade do aparelho e dados de uso do app para selecionar e medir anúncios. Onde a lei exige — hoje o Espaço Econômico Europeu e o Reino Unido —, o consentimento é pedido pelo formulário do próprio Google antes de qualquer anúncio ser solicitado, e a recusa é respeitada: nenhum anúncio é pedido.

A assinatura PRO remove o banner. Com ela nenhum anúncio é solicitado e o SDK de anúncios não chega a ser iniciado.

O Truck GPS não envia à AdMob a sua conta, o seu e-mail nem a sua posição no jogo, e não usa o login para enviar publicidade.

6a. Diagnóstico: falhas, desempenho e uso
O app usa três serviços do Firebase para descobrir problemas que ninguém relata — um GPS que fecha sozinho na estrada não vira reclamação, vira desinstalação:

Crashlytics — relatórios de falha: modelo do aparelho, versão do Android, versão do app e a pilha de chamadas do erro. Junto vai o estado do app no momento: qual jogo, se o plano é FREE ou PRO, se havia conexão com a ponte, se havia rota na tela e o idioma;
Performance Monitoring — tempo de arranque, fluidez do desenho do mapa e quanto demora preparar o pacote de mapa;
Analytics — eventos de uso sem conteúdo pessoal: pareamento concluído, rota calculada (com a distância arredondada em quilômetros) e rota recusada (com o motivo).
Nada disso inclui a sua conta, o seu e-mail, a sua posição no jogo nem o destino do frete. A coleta começa somente depois que você aceita os termos na primeira abertura; antes disso nada é enviado.

7. Acesso, exportação e exclusão
A tela Conta permite baixar os dados mantidos pela API. No Android, o arquivo é salvo em Downloads e pode conter informações da conta e compras; compartilhe-o somente com quem deseja.

A mesma tela permite solicitar exclusão da conta e cancelar a solicitação enquanto disponível. A API informa a data prevista, com janela de 30 dias. Excluir a conta não cancela automaticamente a assinatura na Google Play: gerencie a assinatura na própria loja.

Limpar os dados ou desinstalar remove os dados locais do app; não elimina automaticamente os registros da API ou dos provedores de autenticação e compra. Para dúvidas, correção ou pedidos adicionais, use o contato da seção 1.

8. Atualizações
Este texto vale desde 05/09/2026. Mudanças no tratamento de dados devem ser refletidas aqui e na página pública antes de distribuir a versão correspondente.

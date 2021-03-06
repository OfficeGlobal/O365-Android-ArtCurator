---
page_type: sample
products:
- office-outlook
- office-365
languages:
- java
extensions:
  contentType: samples
  platforms:
  - Android
  createdDate: 6/26/2015 3:03:39 PM
---
# O365-Android-Art-Curator
[![Status da Compilação](https://travis-ci.org/OfficeDev/O365-Android-ArtCurator.svg?branch=master)](https://travis-ci.org/OfficeDev/O365-Android-ArtCurator)


Este exemplo demonstra como usar a API de Email do Outlook para obter emails e anexos do Office 365. Ele foi criado para [iOS](https://github.com/OfficeDev/O365-iOS-ArtCurator), Android, [Web (aplicativo Web Angular)](https://github.com/OfficeDev/O365-Angular-ArtCurator) e [Windows Phone](https://github.com/OfficeDev/O365-WinPhone-ArtCurator). Confira nosso artigo no[Medium](https://medium.com/@iambmelt/14296d0a25be).
<br />
<br />
O exemplo do Art Curator oferece uma maneira diferente de exibir sua caixa de entrada. Imagine que você possui uma empresa que vende camisetas artísticas. Como proprietário da empresa, você recebe muitos emails de artistas com designs que eles querem que você compre. Atualmente, você usa seu cliente de email para abrir todas as mensagens e anexos. Em vez disso, é possível usar o exemplo do Art Curator para obter uma visualização prévia do anexo da caixa de entrada para que você possa escolher os designs de sua preferência. 

Este exemplo demonstra as seguintes operações da API de Email de Serviços do Outlook:
* [Obter pastas](https://msdn.microsoft.com/office/office365/APi/mail-rest-operations#GetFolders)
* [Obter mensagens](https://msdn.microsoft.com/office/office365/APi/mail-rest-operations#Getmessages) (incluindo a filtragem e o uso da seleção)
* [Obter anexos](https://msdn.microsoft.com/office/office365/APi/mail-rest-operations#GetAttachments)
* [Mensagens de atualização](https://msdn.microsoft.com/office/office365/APi/mail-rest-operations#Updatemessages)
* [Criar e enviar mensagens](https://msdn.microsoft.com/office/office365/APi/mail-rest-operations#Sendmessages) (com ou sem um anexo) 

[![Office 365 Android Art Curator](/readme-images/artcurator_android.png)![Clique no exemplo para vê-lo em ação](/readme-images/artcurator_android.png)

Pré-requisitos
==
* [Android Studio](https://developer.android.com/sdk/index.html) ver. 1.0+
* Uma conta do Office 365. Você pode assinar uma [assinatura de Desenvolvedor do Office 365](https://msdn.microsoft.com/en-us/library/office/fp179924.aspx) que inclua os recursos para começar a criar os aplicativos do Office 365.

**Anotação**<br/>
Você também deve garantir que a assinatura do Azure esteja vinculada ao seu locatário do Office 365. Confira a postagem do blog da equipe do Active Directory, [Criar e gerenciar vários Diretórios Ativos do Microsoft Azure](http://blogs.technet.com/b/ad/archive/2013/11/08/creating-and-managing-multiple-windows-azure-active-directories.aspx) para mais instruções. Nesta postagem, a seção Adicionando um novo diretório explica como fazer isso. Para saber mais, leia [Configurar o acesso ao Azure Active Directory para o Site do Desenvolvedor](https://msdn.microsoft.com/office/office365/howto/setup-development-environment#bk_CreateAzureSubscription).

Importar para o Android Studio
==
* Clonar este repositório
* Inicie o Android Studio
  * Importe o projeto (Eclipse ADT, Gradle, etc.) > selecione o ```settings.gradle``` do projeto alvo

Iniciar pela primeira vez
==
Este aplicativo contém informações sobre o aplicativo previamente registradas no Azure com as permissões **Enviar email como um usuário** e **Ler e gravar emails de usuários**.

As informações do aplicativo estão definidas em ```com.microsoft.artcurator.conf.ServiceConstants```.
    
    public static final String CLIENT_ID = "1feaa784-0130-48d9-adeb-776fc65888c5";
    public static final String REDIRECT_URI = "https://useonlytoruntheartcuratorsample/";
        
Para seu próprio aplicativo, [registre o seu aplicativo de cliente nativo no Azure](https://msdn.microsoft.com/library/azure/dn132599.aspx#BKMK_Adding). 

Especifique o URI de redirecionamento ao registrar o seu aplicativo. Em seguida, obtenha a ID do cliente na página **CONFIGURAR**.
O aplicativo *deve* ter as permissões **Enviar email como usuário** e **Ler e escrever email de usuários**.

Para saber mais, confira as Limitações do [exemplo do O365-Android-Connect](https://github.com/OfficeDev/O365-Android-Connect)
==
* Suporte a arquivos além de ```.png``` e ```.jpg```
* Lidar com uma única mensagem de email com vários anexos
* Paginação (recebendo mais de 50 emails)
* Lidar com exclusividade de nome de pasta
* A pasta de envio deve ser uma pasta de nível superior

Perguntas e comentários
==
* Se você tiver problemas para executar este exemplo, [relate um problema](https://github.com/OfficeDev/O365-Android-ArtCurator/issues)
* Para perguntas gerais sobre as APIs do Office 365, poste em [Stack Overflow](http://stackoverflow.com/). Não deixe de marcar as suas perguntas ou comentários com \[Office365] e \[outlook-restapi].

Recursos adicionais
==
* [Introdução às APIs do Office 365 em aplicativos](https://msdn.microsoft.com/en-us/office/office365/howto/getting-started-Office-365-APIs)
* [Centro de Desenvolvimento do Office (Android)](http://dev.office.com/Android)
* [Visão geral da plataforma de APIs do Office 365](http://stackoverflow.com/)
* [Art Curator para iOS](https://github.com/OfficeDev/O365-iOS-ArtCurator)
* [Art Curator para Windows Phone](https://github.com/OfficeDev/O365-WinPhone-ArtCurator)
* [Art Curator para Web (aplicativo Web Angular)](https://github.com/OfficeDev/O365-Angular-ArtCurator)

Direitos autorais
==
Copyright © 2015 Microsoft. Todos os direitos reservados.


Este projeto adotou o [Código de Conduta do Código Aberto da Microsoft](https://opensource.microsoft.com/codeofconduct/). Para saber mais, confira [Perguntas frequentes sobre o Código de Conduta](https://opensource.microsoft.com/codeofconduct/faq/) ou contate [opencode@microsoft.com](mailto:opencode@microsoft.com) se tiver outras dúvidas ou comentários.

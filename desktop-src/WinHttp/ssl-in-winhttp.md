---
description: Службы Microsoft Windows HTTP (WinHTTP) поддерживают транзакции SSL (SSL), включая сертификаты клиентов. В этом разделе объясняются основные понятия, связанные с транзакцией SSL и способами их обработки с помощью WinHTTP.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265000"
---
# <a name="ssl-in-winhttp"></a>SSL в WinHTTP

Службы Microsoft Windows HTTP (WinHTTP) поддерживают транзакции SSL (SSL), включая сертификаты клиентов. В этом разделе объясняются основные понятия, связанные с транзакцией SSL и способами их обработки с помощью WinHTTP.

## <a name="secure-sockets-layer"></a>Протокол SSL

SSL — это установленный стандарт для обеспечения безопасных транзакций HTTP. SSL предоставляет механизм для выполнения до 128-битного шифрования всех транзакций между клиентом и сервером. Он позволяет клиенту проверить принадлежность сервера к доверенному субъекту с помощью сертификатов сервера. Он также позволяет серверу подтвердить удостоверение клиента с помощью сертификатов клиента.

Каждое из этих проблем шифрование, удостоверение сервера и удостоверение клиента согласовывается в подтверждении SSL, которое происходит при первом запросе клиентом ресурса с сервера HTTPS. По сути, клиент и сервер представляют собой список обязательных и предпочтительных параметров. Если вы можете согласовать и выполнить общий набор требований, устанавливается соединение SSL.

WinHTTP предоставляет интерфейс высокого уровня для использования SSL. Хотя сведения о подтверждении SSL и транзакции обрабатываются внутренним образом, службы WinHTTP позволяют извлекать уровни шифрования, указывать протокол безопасности и взаимодействовать с сертификатами сервера и клиента. В следующих разделах приводятся сведения о создании приложений на базе WinHTTP, в которых выбирается версия протокола SSL, изучаются сертификаты сервера и выбираются сертификаты клиента для отправки на HTTPS-серверы.

## <a name="server-certificates"></a>Сертификаты серверов

Сертификаты сервера отправляются с сервера клиенту, чтобы клиент мог получить открытый ключ для сервера и убедиться, что сервер проверен центром сертификации. В сертификатах могут содержаться различные типы данных. Например, сертификат X. 509 включает формат сертификата, серийный номер сертификата, алгоритм, используемый для подписи сертификата, имя центра сертификации (ЦС), который выдал сертификат, имя и открытый ключ сущности, которая запрашивает сертификат, и подпись ЦС.

При использовании прикладного программного интерфейса (API) WinHTTP можно получить сертификат сервера, вызвав [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и указав флаг [**\_ \_ \_ \_ структуры сертификата безопасности параметра WinHTTP**](option-flags.md) . Сертификат сервера возвращается в структуре [**\_ \_ сведений о сертификате WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Если вы предпочитаете получить контекст сертификата, укажите вместо него флаг " [**параметр WinHTTP для \_ \_ \_ сертификата \_ сервера"**](option-flags.md) .

Если сертификат сервера содержит ошибки, сведения об ошибке можно получить в функции обратного вызова состояния. Уведомление [**о \_ \_ \_ \_ сбое обратного вызова WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) указывает на ошибку в сертификате сервера. Параметр *лпвстатусинформатион* содержит один или несколько подробных флагов ошибок. Дополнительные сведения см. в разделе [**\_ о \_ обратном вызове состояния WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .

## <a name="client-certificates"></a>Сертификаты клиента

При подтверждении SSL сервер может потребовать проверки подлинности. Проверка подлинности клиента осуществляется путем предоставления на сервер действительного сертификата клиента. Служба WinHTTP позволяет выбрать и отправить сертификат из локального [*хранилища сертификатов*](glossary.md). В следующих разделах описывается процесс, который предоставляет сертификаты клиента при использовании API WinHTTP или объекта [**WinHttpRequest**](winhttprequest.md) .

### <a name="winhttp-api"></a>API WinHTTP

Как [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , так и [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) могут указывать на то, что запрос был неуспешным, так как HTTPS-сервер требует проверки подлинности. В этих случаях необходимо вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы возвратить сообщение об ошибке \_ \_ \_ сертификат проверки подлинности клиента WinHTTP \_ \_ . При получении этой ошибки используйте соответствующие функции [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) для поиска соответствующего сертификата. Укажите, что этот сертификат следует отправить со следующим запросом, вызвав [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с флагом [**контекста WinHTTP для \_ \_ \_ сертификата \_ клиента**](option-flags.md) .

В следующем примере кода показано, как открыть [*хранилище сертификатов*](glossary.md) и выбрать сертификат на основе имени субъекта после ошибки, \_ необходимой для \_ \_ сертификата проверки подлинности клиента WinHTTP \_ \_ .


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



Перед повторной отправкой запроса, содержащего сертификат клиента, можно определить, приемлем ли поддерживаемый уровень шифрования для вашего приложения. Вызовите [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и укажите [**флаг \_ \_ безопасности для \_ параметра WinHTTP**](option-flags.md) , чтобы определить используемый уровень шифрования.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Получение списка издателей для проверки подлинности клиента SSL

Когда клиентское приложение WinHttp отправляет запрос на защищенный HTTP-сервер, требующий проверки подлинности клиента SSL, служба WinHttp возвращает **сообщение об ошибке " \_ \_ \_ сертификат проверки подлинности клиента \_ \_ WinHTTP** ", необходимый, если приложение не предоставил сертификат клиента. Для компьютеров, работающих под управлением Windows Server 2008 и Windows Vista, служба WinHttp позволяет приложению получить список издателей сертификатов, предоставленный сервером, с помощью запроса на проверку подлинности. В списке издателей указан список центров сертификации (ЦС), которые разрешены сервером для выдачи сертификатов клиентов. Приложение фильтрует список издателей для получения необходимого сертификата.

Клиентское приложение WinHttp получает список поставщиков, когда [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает **ошибку \_ \_ \_ сертификат проверки подлинности \_ \_ клиента WinHTTP**. При возвращении этой ошибки приложение вызывает [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP- \_ \_ Issuer Client \_ CERT \_ \_ List** . Параметр *лпбуффер* должен быть достаточно большим, чтобы содержать указатель на структуру [секпкгконтекст \_ иссуерлистинфоекс](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) . В следующем примере кода показано, как получить список издателей.


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



Сведения в структуре [секпкгконтекст \_ Иссуерлистинфоекс](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *Циссуерс* и *аиссуерс*, можно использовать для поиска сертификата, как показано в примере кода ниже. Дополнительные сведения см. в разделе [**цертфиндчаининсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a>Необязательные SSL-сертификаты клиента

Начиная с Windows Server 2008 и Windows Vista, API WinHttp поддерживает необязательные сертификаты клиента. Когда сервер запрашивает сертификат клиента, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**винхттпреЦиевереспонсе**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает **ошибку, \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP** . Если сервер запрашивает сертификат, но не требует его, приложение может указать этот параметр, чтобы указать, что у него нет сертификата. Сервер может выбрать другую схему проверки подлинности или разрешить анонимный доступ к серверу. Приложение задает **\_ \_ \_ \_ Контекстный макрос WinHTTP No Client** Certificate в параметре *лпбуффер* объекта [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , как показано в следующем примере кода.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Если **\_ \_ \_ \_ контекст сертификата WinHTTP не** задан, а сервер по-прежнему требует сертификат клиента, он может отправить код состояния 403 HTTP. Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .

### <a name="winhttprequest-object"></a>Объект WinHttpRequest

Используйте метод [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) объекта [**WinHttpRequest**](winhttprequest.md) , чтобы выбрать сертификаты клиента для отправки на сервер с запросом. Выберите сертификат, указав строку выбора сертификата с помощью метода [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) . Строка выбора сертификата состоит из расположения сертификата, [*хранилища сертификатов*](glossary.md)и имени субъекта, разделенных символами обратной косой черты. В следующей таблице перечислены компоненты для этой строки выбора.



| Компонент                                                  | Описание                                                                                                                                                                                        | Возможные значения                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Расположение                                                   | Определяет раздел реестра, в котором хранятся сертификаты.                                                                                                                               | Возможные значения: "локальный \_ компьютер", чтобы указать, что [*хранилище сертификатов*](glossary.md) находится на **\_ локальном \_ компьютере hKey**<br/> и "текущий \_ пользователь", чтобы указать, что *хранилище сертификатов* находится под неолицетворенным **\_ текущим пользователем hKey \_ .**<br/> Этот компонент чувствителен к регистру. |
| [*Хранилище сертификатов*](glossary.md) | Указывает имя [*хранилища сертификатов*](glossary.md) , которое содержит соответствующий сертификат.                                                                       | Типичными [*хранилищами сертификатов*](glossary.md) являются «My», «root» и «TrustedPeople». Этот компонент чувствителен к регистру.                                                                                                                                                                                          |
| Имя субъекта                                               | Определяет сертификат в указанном [*хранилище сертификатов*](glossary.md). Выбран первый сертификат, содержащий строку, указанную для этого компонента. | Имя субъекта может быть любой строкой. Пустая строка указывает, что следует использовать первый сертификат в [*хранилище сертификатов*](glossary.md) . Этот компонент не учитывает регистр.                                                                                                                         |



 

Имя и расположение [*хранилища сертификатов*](glossary.md) являются дополнительными компонентами. Однако если указать *хранилище сертификатов*, необходимо также указать расположение этого *хранилища сертификатов*. Расположение по умолчанию — текущий \_ пользователь, а *хранилище сертификатов* по умолчанию — "My".

В следующем примере кода показано, как указать, что сертификат с темой "мой Middle-Tier сертификат" должен быть выбран из [*хранилища сертификатов*](glossary.md) "Личное" в реестре в разделе **hKey \_ локальный \_ компьютер**.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> В некоторых языках обратная косая черта является escape-символом. Не забудьте изменить строку выбора сертификата, чтобы учесть это. Например, в Microsoft JScript вместо одного используется две соседние знаки обратной косой черты.

 

Если не указать сертификат и серверу HTTPS требуется сертификат клиента, служба WinHTTP выбирает первый сертификат в [*хранилище сертификатов*](glossary.md)по умолчанию. Если сертификаты не существуют, возникает ошибка. Если сертификат не принят, сервер возвращает код состояния 403, указывающий, что запрос не может быть выполнен. Затем можно выбрать более подходящий сертификат с помощью [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) и повторно отправить запрос.

 


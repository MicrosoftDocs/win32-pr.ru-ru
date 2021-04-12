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
# <a name="ssl-in-winhttp"></a><span data-ttu-id="4f976-104">SSL в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4f976-104">SSL in WinHTTP</span></span>

<span data-ttu-id="4f976-105">Службы Microsoft Windows HTTP (WinHTTP) поддерживают транзакции SSL (SSL), включая сертификаты клиентов.</span><span class="sxs-lookup"><span data-stu-id="4f976-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="4f976-106">В этом разделе объясняются основные понятия, связанные с транзакцией SSL и способами их обработки с помощью WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4f976-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="4f976-107">Протокол SSL</span><span class="sxs-lookup"><span data-stu-id="4f976-107">Secure Sockets Layer</span></span>

<span data-ttu-id="4f976-108">SSL — это установленный стандарт для обеспечения безопасных транзакций HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f976-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="4f976-109">SSL предоставляет механизм для выполнения до 128-битного шифрования всех транзакций между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="4f976-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="4f976-110">Он позволяет клиенту проверить принадлежность сервера к доверенному субъекту с помощью сертификатов сервера.</span><span class="sxs-lookup"><span data-stu-id="4f976-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="4f976-111">Он также позволяет серверу подтвердить удостоверение клиента с помощью сертификатов клиента.</span><span class="sxs-lookup"><span data-stu-id="4f976-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="4f976-112">Каждое из этих проблем шифрование, удостоверение сервера и удостоверение клиента согласовывается в подтверждении SSL, которое происходит при первом запросе клиентом ресурса с сервера HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4f976-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="4f976-113">По сути, клиент и сервер представляют собой список обязательных и предпочтительных параметров.</span><span class="sxs-lookup"><span data-stu-id="4f976-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="4f976-114">Если вы можете согласовать и выполнить общий набор требований, устанавливается соединение SSL.</span><span class="sxs-lookup"><span data-stu-id="4f976-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="4f976-115">WinHTTP предоставляет интерфейс высокого уровня для использования SSL.</span><span class="sxs-lookup"><span data-stu-id="4f976-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="4f976-116">Хотя сведения о подтверждении SSL и транзакции обрабатываются внутренним образом, службы WinHTTP позволяют извлекать уровни шифрования, указывать протокол безопасности и взаимодействовать с сертификатами сервера и клиента.</span><span class="sxs-lookup"><span data-stu-id="4f976-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="4f976-117">В следующих разделах приводятся сведения о создании приложений на базе WinHTTP, в которых выбирается версия протокола SSL, изучаются сертификаты сервера и выбираются сертификаты клиента для отправки на HTTPS-серверы.</span><span class="sxs-lookup"><span data-stu-id="4f976-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="4f976-118">Сертификаты серверов</span><span class="sxs-lookup"><span data-stu-id="4f976-118">Server Certificates</span></span>

<span data-ttu-id="4f976-119">Сертификаты сервера отправляются с сервера клиенту, чтобы клиент мог получить открытый ключ для сервера и убедиться, что сервер проверен центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="4f976-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="4f976-120">В сертификатах могут содержаться различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="4f976-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="4f976-121">Например, сертификат X. 509 включает формат сертификата, серийный номер сертификата, алгоритм, используемый для подписи сертификата, имя центра сертификации (ЦС), который выдал сертификат, имя и открытый ключ сущности, которая запрашивает сертификат, и подпись ЦС.</span><span class="sxs-lookup"><span data-stu-id="4f976-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="4f976-122">При использовании прикладного программного интерфейса (API) WinHTTP можно получить сертификат сервера, вызвав [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и указав флаг [**\_ \_ \_ \_ структуры сертификата безопасности параметра WinHTTP**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="4f976-123">Сертификат сервера возвращается в структуре [**\_ \_ сведений о сертификате WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) .</span><span class="sxs-lookup"><span data-stu-id="4f976-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="4f976-124">Если вы предпочитаете получить контекст сертификата, укажите вместо него флаг " [**параметр WinHTTP для \_ \_ \_ сертификата \_ сервера"**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="4f976-125">Если сертификат сервера содержит ошибки, сведения об ошибке можно получить в функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="4f976-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="4f976-126">Уведомление [**о \_ \_ \_ \_ сбое обратного вызова WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) указывает на ошибку в сертификате сервера.</span><span class="sxs-lookup"><span data-stu-id="4f976-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="4f976-127">Параметр *лпвстатусинформатион* содержит один или несколько подробных флагов ошибок.</span><span class="sxs-lookup"><span data-stu-id="4f976-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="4f976-128">Дополнительные сведения см. в разделе [**\_ о \_ обратном вызове состояния WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="4f976-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="4f976-129">Сертификаты клиента</span><span class="sxs-lookup"><span data-stu-id="4f976-129">Client Certificates</span></span>

<span data-ttu-id="4f976-130">При подтверждении SSL сервер может потребовать проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f976-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="4f976-131">Проверка подлинности клиента осуществляется путем предоставления на сервер действительного сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="4f976-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="4f976-132">Служба WinHTTP позволяет выбрать и отправить сертификат из локального [*хранилища сертификатов*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4f976-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f976-133">В следующих разделах описывается процесс, который предоставляет сертификаты клиента при использовании API WinHTTP или объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="4f976-134">API WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4f976-134">WinHTTP API</span></span>

<span data-ttu-id="4f976-135">Как [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , так и [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) могут указывать на то, что запрос был неуспешным, так как HTTPS-сервер требует проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f976-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="4f976-136">В этих случаях необходимо вызвать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы возвратить сообщение об ошибке \_ \_ \_ сертификат проверки подлинности клиента WinHTTP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4f976-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="4f976-137">При получении этой ошибки используйте соответствующие функции [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) для поиска соответствующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="4f976-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="4f976-138">Укажите, что этот сертификат следует отправить со следующим запросом, вызвав [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с флагом [**контекста WinHTTP для \_ \_ \_ сертификата \_ клиента**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="4f976-139">В следующем примере кода показано, как открыть [*хранилище сертификатов*](glossary.md) и выбрать сертификат на основе имени субъекта после ошибки, \_ необходимой для \_ \_ сертификата проверки подлинности клиента WinHTTP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4f976-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


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



<span data-ttu-id="4f976-140">Перед повторной отправкой запроса, содержащего сертификат клиента, можно определить, приемлем ли поддерживаемый уровень шифрования для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="4f976-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="4f976-141">Вызовите [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и укажите [**флаг \_ \_ безопасности для \_ параметра WinHTTP**](option-flags.md) , чтобы определить используемый уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="4f976-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="4f976-142">Получение списка издателей для проверки подлинности клиента SSL</span><span class="sxs-lookup"><span data-stu-id="4f976-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="4f976-143">Когда клиентское приложение WinHttp отправляет запрос на защищенный HTTP-сервер, требующий проверки подлинности клиента SSL, служба WinHttp возвращает **сообщение об ошибке " \_ \_ \_ сертификат проверки подлинности клиента \_ \_ WinHTTP** ", необходимый, если приложение не предоставил сертификат клиента.</span><span class="sxs-lookup"><span data-stu-id="4f976-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="4f976-144">Для компьютеров, работающих под управлением Windows Server 2008 и Windows Vista, служба WinHttp позволяет приложению получить список издателей сертификатов, предоставленный сервером, с помощью запроса на проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f976-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="4f976-145">В списке издателей указан список центров сертификации (ЦС), которые разрешены сервером для выдачи сертификатов клиентов.</span><span class="sxs-lookup"><span data-stu-id="4f976-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="4f976-146">Приложение фильтрует список издателей для получения необходимого сертификата.</span><span class="sxs-lookup"><span data-stu-id="4f976-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="4f976-147">Клиентское приложение WinHttp получает список поставщиков, когда [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает **ошибку \_ \_ \_ сертификат проверки подлинности \_ \_ клиента WinHTTP**.</span><span class="sxs-lookup"><span data-stu-id="4f976-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="4f976-148">При возвращении этой ошибки приложение вызывает [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP- \_ \_ Issuer Client \_ CERT \_ \_ List** .</span><span class="sxs-lookup"><span data-stu-id="4f976-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="4f976-149">Параметр *лпбуффер* должен быть достаточно большим, чтобы содержать указатель на структуру [секпкгконтекст \_ иссуерлистинфоекс](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) .</span><span class="sxs-lookup"><span data-stu-id="4f976-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="4f976-150">В следующем примере кода показано, как получить список издателей.</span><span class="sxs-lookup"><span data-stu-id="4f976-150">The following code example shows how to retrieve the issuer list.</span></span>


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



<span data-ttu-id="4f976-151">Сведения в структуре [секпкгконтекст \_ Иссуерлистинфоекс](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *Циссуерс* и *аиссуерс*, можно использовать для поиска сертификата, как показано в примере кода ниже.</span><span class="sxs-lookup"><span data-stu-id="4f976-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="4f976-152">Дополнительные сведения см. в разделе [**цертфиндчаининсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="4f976-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


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



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="4f976-153">Необязательные SSL-сертификаты клиента</span><span class="sxs-lookup"><span data-stu-id="4f976-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="4f976-154">Начиная с Windows Server 2008 и Windows Vista, API WinHttp поддерживает необязательные сертификаты клиента.</span><span class="sxs-lookup"><span data-stu-id="4f976-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="4f976-155">Когда сервер запрашивает сертификат клиента, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**винхттпреЦиевереспонсе**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает **ошибку, \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="4f976-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="4f976-156">Если сервер запрашивает сертификат, но не требует его, приложение может указать этот параметр, чтобы указать, что у него нет сертификата.</span><span class="sxs-lookup"><span data-stu-id="4f976-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="4f976-157">Сервер может выбрать другую схему проверки подлинности или разрешить анонимный доступ к серверу.</span><span class="sxs-lookup"><span data-stu-id="4f976-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="4f976-158">Приложение задает **\_ \_ \_ \_ Контекстный макрос WinHTTP No Client** Certificate в параметре *лпбуффер* объекта [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="4f976-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="4f976-159">Если **\_ \_ \_ \_ контекст сертификата WinHTTP не** задан, а сервер по-прежнему требует сертификат клиента, он может отправить код состояния 403 HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f976-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="4f976-160">Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .</span><span class="sxs-lookup"><span data-stu-id="4f976-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="4f976-161">Объект WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="4f976-161">WinHttpRequest Object</span></span>

<span data-ttu-id="4f976-162">Используйте метод [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) объекта [**WinHttpRequest**](winhttprequest.md) , чтобы выбрать сертификаты клиента для отправки на сервер с запросом.</span><span class="sxs-lookup"><span data-stu-id="4f976-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="4f976-163">Выберите сертификат, указав строку выбора сертификата с помощью метода [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="4f976-164">Строка выбора сертификата состоит из расположения сертификата, [*хранилища сертификатов*](glossary.md)и имени субъекта, разделенных символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="4f976-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="4f976-165">В следующей таблице перечислены компоненты для этой строки выбора.</span><span class="sxs-lookup"><span data-stu-id="4f976-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="4f976-166">Компонент</span><span class="sxs-lookup"><span data-stu-id="4f976-166">Component</span></span>                                                  | <span data-ttu-id="4f976-167">Описание</span><span class="sxs-lookup"><span data-stu-id="4f976-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="4f976-168">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4f976-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f976-169">Расположение</span><span class="sxs-lookup"><span data-stu-id="4f976-169">Location</span></span>                                                   | <span data-ttu-id="4f976-170">Определяет раздел реестра, в котором хранятся сертификаты.</span><span class="sxs-lookup"><span data-stu-id="4f976-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="4f976-171">Возможные значения: "локальный \_ компьютер", чтобы указать, что [*хранилище сертификатов*](glossary.md) находится на **\_ локальном \_ компьютере hKey**</span><span class="sxs-lookup"><span data-stu-id="4f976-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="4f976-172">и "текущий \_ пользователь", чтобы указать, что *хранилище сертификатов* находится под неолицетворенным **\_ текущим пользователем hKey \_ .**</span><span class="sxs-lookup"><span data-stu-id="4f976-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="4f976-173">Этот компонент чувствителен к регистру.</span><span class="sxs-lookup"><span data-stu-id="4f976-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="4f976-174">*Хранилище сертификатов*</span><span class="sxs-lookup"><span data-stu-id="4f976-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="4f976-175">Указывает имя [*хранилища сертификатов*](glossary.md) , которое содержит соответствующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="4f976-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="4f976-176">Типичными [*хранилищами сертификатов*](glossary.md) являются «My», «root» и «TrustedPeople».</span><span class="sxs-lookup"><span data-stu-id="4f976-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="4f976-177">Этот компонент чувствителен к регистру.</span><span class="sxs-lookup"><span data-stu-id="4f976-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="4f976-178">Имя субъекта</span><span class="sxs-lookup"><span data-stu-id="4f976-178">Subject name</span></span>                                               | <span data-ttu-id="4f976-179">Определяет сертификат в указанном [*хранилище сертификатов*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4f976-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f976-180">Выбран первый сертификат, содержащий строку, указанную для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="4f976-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="4f976-181">Имя субъекта может быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="4f976-181">The subject name can be any string.</span></span> <span data-ttu-id="4f976-182">Пустая строка указывает, что следует использовать первый сертификат в [*хранилище сертификатов*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="4f976-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="4f976-183">Этот компонент не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="4f976-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="4f976-184">Имя и расположение [*хранилища сертификатов*](glossary.md) являются дополнительными компонентами.</span><span class="sxs-lookup"><span data-stu-id="4f976-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="4f976-185">Однако если указать *хранилище сертификатов*, необходимо также указать расположение этого *хранилища сертификатов*.</span><span class="sxs-lookup"><span data-stu-id="4f976-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="4f976-186">Расположение по умолчанию — текущий \_ пользователь, а *хранилище сертификатов* по умолчанию — "My".</span><span class="sxs-lookup"><span data-stu-id="4f976-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="4f976-187">В следующем примере кода показано, как указать, что сертификат с темой "мой Middle-Tier сертификат" должен быть выбран из [*хранилища сертификатов*](glossary.md) "Личное" в реестре в разделе **hKey \_ локальный \_ компьютер**.</span><span class="sxs-lookup"><span data-stu-id="4f976-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="4f976-188">В некоторых языках обратная косая черта является escape-символом.</span><span class="sxs-lookup"><span data-stu-id="4f976-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="4f976-189">Не забудьте изменить строку выбора сертификата, чтобы учесть это.</span><span class="sxs-lookup"><span data-stu-id="4f976-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="4f976-190">Например, в Microsoft JScript вместо одного используется две соседние знаки обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="4f976-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="4f976-191">Если не указать сертификат и серверу HTTPS требуется сертификат клиента, служба WinHTTP выбирает первый сертификат в [*хранилище сертификатов*](glossary.md)по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f976-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="4f976-192">Если сертификаты не существуют, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="4f976-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="4f976-193">Если сертификат не принят, сервер возвращает код состояния 403, указывающий, что запрос не может быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="4f976-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="4f976-194">Затем можно выбрать более подходящий сертификат с помощью [**сетклиентцертификате**](iwinhttprequest-setclientcertificate.md) и повторно отправить запрос.</span><span class="sxs-lookup"><span data-stu-id="4f976-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 


---
description: Следует соблюдать осторожность при использовании поставщика поддержки безопасности Kerberos (SSP), если требуется взаимодействие с GSSAPI.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Взаимодействие SSPI/Kerberos с GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808350"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="42fa5-103">Взаимодействие SSPI/Kerberos с GSSAPI</span><span class="sxs-lookup"><span data-stu-id="42fa5-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="42fa5-104">Следует соблюдать осторожность при использовании [*поставщика поддержки безопасности*](../secgloss/s-gly.md) [*Kerberos*](../secgloss/k-gly.md) (SSP), если требуется взаимодействие с GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="42fa5-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="42fa5-105">Следующие соглашения о коде позволяют обеспечить взаимодействие с приложениями на основе GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="42fa5-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="42fa5-106">Имена, совместимые с Windows</span><span class="sxs-lookup"><span data-stu-id="42fa5-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="42fa5-107">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="42fa5-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="42fa5-108">Целостность и конфиденциальность сообщений</span><span class="sxs-lookup"><span data-stu-id="42fa5-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="42fa5-109">Пример кода можно найти в пакете SDK для платформы "примеры \\ безопасности \\ SSPI \\ GSS".</span><span class="sxs-lookup"><span data-stu-id="42fa5-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="42fa5-110">Кроме того, эквивалентный пример для UNIX распространяется в дистрибутивах MIT и Хеимдал Kerberos, а также в клиенте и на сервере GSS.</span><span class="sxs-lookup"><span data-stu-id="42fa5-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="42fa5-111">Имена Windows-Compatible</span><span class="sxs-lookup"><span data-stu-id="42fa5-111">Windows-Compatible Names</span></span>

<span data-ttu-id="42fa5-112">Функции GSSAPI используют формат имени, известный как \_ имя службы NT для GSS \_ \_ , как указано в RFC.</span><span class="sxs-lookup"><span data-stu-id="42fa5-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="42fa5-113">Например, sample@host.dom.com — это имя, которое можно использовать в приложении на основе GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="42fa5-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="42fa5-114">Операционная система Windows не распознает \_ \_ Формат имени службы NT GSS \_ , а полное [*имя субъекта-службы*](../secgloss/s-gly.md), например sample/host.dom.com@REALM , должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="42fa5-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="42fa5-115">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="42fa5-115">Authentication</span></span>

<span data-ttu-id="42fa5-116">Проверка подлинности обычно обрабатывается при первой установке соединения между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="42fa5-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="42fa5-117">В этом примере клиент использует [*интерфейс поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI), а сервер использует GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="42fa5-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="42fa5-118">**Настройка проверки подлинности в клиенте SSPI**</span><span class="sxs-lookup"><span data-stu-id="42fa5-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="42fa5-119">Получите исходящие [*учетные данные*](../secgloss/c-gly.md) с помощью [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="42fa5-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="42fa5-120">Создайте имя службы с **\_ именем импорта GSS \_ ()** и получите входящие учетные данные с помощью **GSS Get \_ \_ cred**.</span><span class="sxs-lookup"><span data-stu-id="42fa5-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="42fa5-121">Получите маркер проверки подлинности для отправки на сервер с помощью [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="42fa5-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="42fa5-122">Отправьте токен на сервер.</span><span class="sxs-lookup"><span data-stu-id="42fa5-122">Send the token to the server.</span></span>

<span data-ttu-id="42fa5-123">**Настройка проверки подлинности на сервере GSSAPI**</span><span class="sxs-lookup"><span data-stu-id="42fa5-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="42fa5-124">Проанализируйте сообщение от клиента, чтобы извлечь маркер безопасности.</span><span class="sxs-lookup"><span data-stu-id="42fa5-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="42fa5-125">Используйте функцию **\_ \_ \_ контекста GSS Accept в секунду** , передав маркер в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="42fa5-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="42fa5-126">Проанализируйте сообщение с сервера, чтобы извлечь маркер безопасности.</span><span class="sxs-lookup"><span data-stu-id="42fa5-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="42fa5-127">Передайте этот маркер безопасности в [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="42fa5-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="42fa5-128">Отправка маркера ответа клиенту.</span><span class="sxs-lookup"><span data-stu-id="42fa5-128">Send a response token to the client.</span></span>

    <span data-ttu-id="42fa5-129">Функция **\_ контекста "Accept- \_ sec \_** " в GSS может возвращать маркер, который можно отправить обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="42fa5-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="42fa5-130">Если необходимо продолжить, отправьте на сервер маркер ответа. в противном случае Настройка проверки подлинности будет завершена.</span><span class="sxs-lookup"><span data-stu-id="42fa5-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="42fa5-131">Если необходимо продолжить, дождитесь следующего токена от клиента. в противном случае Настройка проверки подлинности будет завершена.</span><span class="sxs-lookup"><span data-stu-id="42fa5-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="42fa5-132">Целостность и конфиденциальность сообщений</span><span class="sxs-lookup"><span data-stu-id="42fa5-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="42fa5-133">Большинство приложений на основе GSSAPI используют функцию **\_ обертывания GSS** для подписи сообщения перед его отправкой.</span><span class="sxs-lookup"><span data-stu-id="42fa5-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="42fa5-134">И наоборот, функция **\_ распаковки GSS** проверяет подпись.</span><span class="sxs-lookup"><span data-stu-id="42fa5-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="42fa5-135">**GSS \_ Оболочка** доступна в версии 2,0 API и теперь широко используется и указывается в стандартах Интернета, описывающих использование GSSAPI для добавления безопасности в протоколы.</span><span class="sxs-lookup"><span data-stu-id="42fa5-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="42fa5-136">Ранее функции GSS **сигнмессаже** и **сеалмессаже** использовались для [*обеспечения целостности*](../secgloss/i-gly.md) и [*конфиденциальности*](../secgloss/p-gly.md)сообщений.</span><span class="sxs-lookup"><span data-stu-id="42fa5-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="42fa5-137">**GSS \_** Разметка Wrap и **GSS \_** используется как для обеспечения целостности данных, так и для обеспечения конфиденциальности с использованием конфиденциальности, управляемой значением \_ аргумента флага "conf".</span><span class="sxs-lookup"><span data-stu-id="42fa5-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="42fa5-138">Если указан протокол на основе GSSAPI, который должен использовать **GSS \_ Get \_ MIC** и **GSS проверять функции \_ \_ MIC** , правильные функции SSPI будут [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span><span class="sxs-lookup"><span data-stu-id="42fa5-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="42fa5-139">Имейте в виду, что **макесигнатуре** и **VerifySignature** не будут взаимодействовать с использованием **\_ оболочки GSS** \_ , если флагу CONF присвоено значение 0 или если для параметра- **\_ оболочки GSS** задано пометка.</span><span class="sxs-lookup"><span data-stu-id="42fa5-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="42fa5-140">Это справедливо и для смешения [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) , установленного только для сигнатур, и для **GSS \_ проверять \_ микрофон**.</span><span class="sxs-lookup"><span data-stu-id="42fa5-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="42fa5-141">Не используйте функции [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) или [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , если для не вызывается функция **\_ распаковки GSS** и **GSS \_** .</span><span class="sxs-lookup"><span data-stu-id="42fa5-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="42fa5-142">SSPI-эквивалент для **GSS \_ Wrap** — это [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) для обеспечения целостности и конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="42fa5-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="42fa5-143">В следующем примере показано использование [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) для подписывания данных, которые будут проверены при **\_ распаковке GSS**.</span><span class="sxs-lookup"><span data-stu-id="42fa5-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="42fa5-144">В клиенте SSPI:</span><span class="sxs-lookup"><span data-stu-id="42fa5-144">In the SSPI client:</span></span>


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



<span data-ttu-id="42fa5-145">На сервере GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="42fa5-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="42fa5-146">SSPI, эквивалентный для **GSS \_ Unwrap** , — это [**декриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="42fa5-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="42fa5-147">Ниже приведен пример, демонстрирующий использование **декриптмессаже (Kerberos)** для расшифровки данных, которые были зашифрованы с помощью **GSS- \_ оболочки**.</span><span class="sxs-lookup"><span data-stu-id="42fa5-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="42fa5-148">На сервере GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="42fa5-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="42fa5-149">В клиенте SSPI:</span><span class="sxs-lookup"><span data-stu-id="42fa5-149">In the SSPI client:</span></span>


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 

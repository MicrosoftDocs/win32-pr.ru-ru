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
# <a name="sspikerberos-interoperability-with-gssapi"></a>Взаимодействие SSPI/Kerberos с GSSAPI

Следует соблюдать осторожность при использовании [*поставщика поддержки безопасности*](../secgloss/s-gly.md) [*Kerberos*](../secgloss/k-gly.md) (SSP), если требуется взаимодействие с GSSAPI. Следующие соглашения о коде позволяют обеспечить взаимодействие с приложениями на основе GSSAPI:

-   [Имена, совместимые с Windows](#windows-compatible-names)
-   [Аутентификация](#authentication)
-   [Целостность и конфиденциальность сообщений](#message-integrity-and-privacy)

Пример кода можно найти в пакете SDK для платформы "примеры \\ безопасности \\ SSPI \\ GSS". Кроме того, эквивалентный пример для UNIX распространяется в дистрибутивах MIT и Хеимдал Kerberos, а также в клиенте и на сервере GSS.

## <a name="windows-compatible-names"></a>Имена Windows-Compatible

Функции GSSAPI используют формат имени, известный как \_ имя службы NT для GSS \_ \_ , как указано в RFC. Например, sample@host.dom.com — это имя, которое можно использовать в приложении на основе GSSAPI. Операционная система Windows не распознает \_ \_ Формат имени службы NT GSS \_ , а полное [*имя субъекта-службы*](../secgloss/s-gly.md), например sample/host.dom.com@REALM , должно использоваться.

## <a name="authentication"></a>Аутентификация

Проверка подлинности обычно обрабатывается при первой установке соединения между клиентом и сервером. В этом примере клиент использует [*интерфейс поставщика поддержки безопасности*](../secgloss/s-gly.md) (SSPI), а сервер использует GSSAPI.

**Настройка проверки подлинности в клиенте SSPI**

1.  Получите исходящие [*учетные данные*](../secgloss/c-gly.md) с помощью [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Создайте имя службы с **\_ именем импорта GSS \_ ()** и получите входящие учетные данные с помощью **GSS Get \_ \_ cred**.
3.  Получите маркер проверки подлинности для отправки на сервер с помощью [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
4.  Отправьте токен на сервер.

**Настройка проверки подлинности на сервере GSSAPI**

1.  Проанализируйте сообщение от клиента, чтобы извлечь маркер безопасности. Используйте функцию **\_ \_ \_ контекста GSS Accept в секунду** , передав маркер в качестве аргумента.
2.  Проанализируйте сообщение с сервера, чтобы извлечь маркер безопасности. Передайте этот маркер безопасности в [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Отправка маркера ответа клиенту.

    Функция **\_ контекста "Accept- \_ sec \_** " в GSS может возвращать маркер, который можно отправить обратно клиенту.

4.  Если необходимо продолжить, отправьте на сервер маркер ответа. в противном случае Настройка проверки подлинности будет завершена.
5.  Если необходимо продолжить, дождитесь следующего токена от клиента. в противном случае Настройка проверки подлинности будет завершена.

## <a name="message-integrity-and-privacy"></a>Целостность и конфиденциальность сообщений

Большинство приложений на основе GSSAPI используют функцию **\_ обертывания GSS** для подписи сообщения перед его отправкой. И наоборот, функция **\_ распаковки GSS** проверяет подпись. **GSS \_ Оболочка** доступна в версии 2,0 API и теперь широко используется и указывается в стандартах Интернета, описывающих использование GSSAPI для добавления безопасности в протоколы. Ранее функции GSS **сигнмессаже** и **сеалмессаже** использовались для [*обеспечения целостности*](../secgloss/i-gly.md) и [*конфиденциальности*](../secgloss/p-gly.md)сообщений. **GSS \_** Разметка Wrap и **GSS \_** используется как для обеспечения целостности данных, так и для обеспечения конфиденциальности с использованием конфиденциальности, управляемой значением \_ аргумента флага "conf".

Если указан протокол на основе GSSAPI, который должен использовать **GSS \_ Get \_ MIC** и **GSS проверять функции \_ \_ MIC** , правильные функции SSPI будут [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). Имейте в виду, что **макесигнатуре** и **VerifySignature** не будут взаимодействовать с использованием **\_ оболочки GSS** \_ , если флагу CONF присвоено значение 0 или если для параметра- **\_ оболочки GSS** задано пометка. Это справедливо и для смешения [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) , установленного только для сигнатур, и для **GSS \_ проверять \_ микрофон**.

> [!Note]  
> Не используйте функции [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) или [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , если для не вызывается функция **\_ распаковки GSS** и **GSS \_** .

 

SSPI-эквивалент для **GSS \_ Wrap** — это [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) для обеспечения целостности и конфиденциальности.

В следующем примере показано использование [**енкриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) для подписывания данных, которые будут проверены при **\_ распаковке GSS**.

В клиенте SSPI:


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



На сервере GSSAPI:


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



SSPI, эквивалентный для **GSS \_ Unwrap** , — это [**декриптмессаже (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Ниже приведен пример, демонстрирующий использование **декриптмессаже (Kerberos)** для расшифровки данных, которые были зашифрованы с помощью **GSS- \_ оболочки**.

На сервере GSSAPI:


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



В клиенте SSPI:


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



 

 

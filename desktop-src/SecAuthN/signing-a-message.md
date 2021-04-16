---
description: Когда клиент и сервер завершают настройку контекста безопасности, можно использовать функции поддержки сообщений.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Подписывание сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664167"
---
# <a name="signing-a-message"></a>Подписывание сообщения

Когда клиент и сервер завершают настройку [*контекста безопасности*](../secgloss/s-gly.md), можно использовать функции поддержки сообщений. Клиент и сервер используют маркер контекста безопасности, созданный при установлении сеанса для вызова функций [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . Маркер контекста можно использовать с [**енкриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) и [**декриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) для [*обеспечения конфиденциальности*](../secgloss/p-gly.md)связи.

В следующем примере показана клиентская часть, создающая подписанное сообщение для отправки на сервер. Перед вызовом [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature)клиент вызывает [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) с структурой [**\_ размеров секпкгконтекст**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) , чтобы определить длину буфера, необходимого для хранения подписи сообщения. Если элемент **кбмакссигнатуре** равен нулю, [*пакет безопасности*](../secgloss/s-gly.md) не поддерживает подписывание сообщений. В противном случае этот элемент указывает размер буфера, выделяемого для получения подписи.

В примере предполагается, что инициализирована переменная **сечандле** с именем *Фконтекст* и структура **сокета** с именем *s* . Объявления и инициации этих переменных см. в разделе [Использование SSPI с клиентом сокетов Windows](using-sspi-with-a-windows-sockets-client.md) и [Использование SSPI с сервером Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Этот пример включает вызовы функций в Secur32. lib, которые должны быть включены в библиотеки ссылок.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



[**Макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) возвращает **значение true** , если контекст настроен для разрешения подписывания сообщений и если дескриптор входного буфера имеет правильный формат. После подписания сообщения сообщение и подпись с их длиной отправляются на удаленный компьютер.

> [!Note]  
> Содержимое данных структур [**pvbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) отправляется, а не сами структуры **Pvbuffer** и структура [**секбуффердеск**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) . Новые структуры **pvbuffer** и новая структура **секбуффердеск** создаются принимающим приложением для проверки подписи.

 

 

 

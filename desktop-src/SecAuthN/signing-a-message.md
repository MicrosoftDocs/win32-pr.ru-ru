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
# <a name="signing-a-message"></a><span data-ttu-id="ad428-103">Подписывание сообщения</span><span class="sxs-lookup"><span data-stu-id="ad428-103">Signing a Message</span></span>

<span data-ttu-id="ad428-104">Когда клиент и сервер завершают настройку [*контекста безопасности*](../secgloss/s-gly.md), можно использовать функции поддержки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad428-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="ad428-105">Клиент и сервер используют маркер контекста безопасности, созданный при установлении сеанса для вызова функций [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="ad428-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="ad428-106">Маркер контекста можно использовать с [**енкриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) и [**декриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) для [*обеспечения конфиденциальности*](../secgloss/p-gly.md)связи.</span><span class="sxs-lookup"><span data-stu-id="ad428-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="ad428-107">В следующем примере показана клиентская часть, создающая подписанное сообщение для отправки на сервер.</span><span class="sxs-lookup"><span data-stu-id="ad428-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="ad428-108">Перед вызовом [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature)клиент вызывает [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) с структурой [**\_ размеров секпкгконтекст**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) , чтобы определить длину буфера, необходимого для хранения подписи сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad428-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="ad428-109">Если элемент **кбмакссигнатуре** равен нулю, [*пакет безопасности*](../secgloss/s-gly.md) не поддерживает подписывание сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad428-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="ad428-110">В противном случае этот элемент указывает размер буфера, выделяемого для получения подписи.</span><span class="sxs-lookup"><span data-stu-id="ad428-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="ad428-111">В примере предполагается, что инициализирована переменная **сечандле** с именем *Фконтекст* и структура **сокета** с именем *s* .</span><span class="sxs-lookup"><span data-stu-id="ad428-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="ad428-112">Объявления и инициации этих переменных см. в разделе [Использование SSPI с клиентом сокетов Windows](using-sspi-with-a-windows-sockets-client.md) и [Использование SSPI с сервером Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="ad428-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="ad428-113">Этот пример включает вызовы функций в Secur32. lib, которые должны быть включены в библиотеки ссылок.</span><span class="sxs-lookup"><span data-stu-id="ad428-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


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



<span data-ttu-id="ad428-114">[**Макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) возвращает **значение true** , если контекст настроен для разрешения подписывания сообщений и если дескриптор входного буфера имеет правильный формат.</span><span class="sxs-lookup"><span data-stu-id="ad428-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="ad428-115">После подписания сообщения сообщение и подпись с их длиной отправляются на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="ad428-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="ad428-116">Содержимое данных структур [**pvbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) отправляется, а не сами структуры **Pvbuffer** и структура [**секбуффердеск**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="ad428-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="ad428-117">Новые структуры **pvbuffer** и новая структура **секбуффердеск** создаются принимающим приложением для проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="ad428-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 

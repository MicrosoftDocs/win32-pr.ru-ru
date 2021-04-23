---
description: Объясняет, как установить контекст безопасности, защищающий взаимодействие между клиентом и сервером.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Создание контекста безопасности безопасного канала Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647363"
---
# <a name="creating-an-schannel-security-context"></a><span data-ttu-id="4e44a-103">Создание контекста безопасности безопасного канала Schannel</span><span class="sxs-lookup"><span data-stu-id="4e44a-103">Creating an Schannel Security Context</span></span>

<span data-ttu-id="4e44a-104">Чтобы установить [*контекст безопасности*](/windows/desktop/SecGloss/s-gly) , который будет защищать обмен данными между клиентом и сервером, необходимо принять участие в следующем процессе обмена информацией:</span><span class="sxs-lookup"><span data-stu-id="4e44a-104">To establish a [*security context*](/windows/desktop/SecGloss/s-gly) that will protect communications between a client and server, both must participate in the following information exchange process:</span></span>

## <a name="client"></a><span data-ttu-id="4e44a-105">Клиент</span><span class="sxs-lookup"><span data-stu-id="4e44a-105">Client</span></span>

1.  <span data-ttu-id="4e44a-106">Клиент вызывает функцию [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="4e44a-106">The client calls the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>
2.  <span data-ttu-id="4e44a-107">Schannel начинает создавать контекст безопасности в соответствии с правилами выбранного протокола безопасности.</span><span class="sxs-lookup"><span data-stu-id="4e44a-107">Schannel begins creating a security context according to the rules of the selected security protocol.</span></span> <span data-ttu-id="4e44a-108">Код возврата функции указывает, должен ли клиент повторно вызывать функцию.</span><span class="sxs-lookup"><span data-stu-id="4e44a-108">The function's return code indicates whether the client must call the function again.</span></span> <span data-ttu-id="4e44a-109">[**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) может возвращать маркер, представляющий контекст.</span><span class="sxs-lookup"><span data-stu-id="4e44a-109">[**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) may return a token that represents the context.</span></span>
3.  <span data-ttu-id="4e44a-110">Если маркер был возвращен, клиент отправляет его на сервер.</span><span class="sxs-lookup"><span data-stu-id="4e44a-110">If a token was returned, the client sends it to the server.</span></span>
4.  <span data-ttu-id="4e44a-111">Когда [**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) возвращает значение \_ \_ в секунду, то клиент выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e44a-111">When [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) returns SEC\_E\_OK, the client is done.</span></span> <span data-ttu-id="4e44a-112">Если функция возвращает секунды \_ \_ \_ , то клиент должен подождать, пока сервер отправит ему маркер.</span><span class="sxs-lookup"><span data-stu-id="4e44a-112">If the function returns SEC\_I\_CONTINUE\_NEEDED, the client must wait for the server to send it a token.</span></span> <span data-ttu-id="4e44a-113">Если у клиента есть маркер с сервера, он должен снова вызвать [*функцию*](/windows/desktop/SecGloss/c-gly) **InitializeSecurityContext (General)** .</span><span class="sxs-lookup"><span data-stu-id="4e44a-113">When the client has the token from the server, it must call the **InitializeSecurityContext (General)** [*function*](/windows/desktop/SecGloss/c-gly) again.</span></span> <span data-ttu-id="4e44a-114">(Вернитесь к шагу 2.)</span><span class="sxs-lookup"><span data-stu-id="4e44a-114">(Return to step 2.)</span></span>

## <a name="server"></a><span data-ttu-id="4e44a-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="4e44a-115">Server</span></span>

1.  <span data-ttu-id="4e44a-116">Сервер ожидает отправки клиентом сообщения, содержащего маркер безопасности.</span><span class="sxs-lookup"><span data-stu-id="4e44a-116">The server waits for a client to send a message that contains a security token.</span></span> <span data-ttu-id="4e44a-117">Сервер передает маркер, полученный от клиента, в функцию [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="4e44a-117">The server passes the token received from the client into the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>
2.  <span data-ttu-id="4e44a-118">Schannel строится на частичном контексте безопасности, представленном токеном.</span><span class="sxs-lookup"><span data-stu-id="4e44a-118">Schannel builds on the partial security context represented by the token.</span></span> <span data-ttu-id="4e44a-119">Schannel возвращает маркер серверу и код возврата, указывающий, должен ли сервер повторно вызывать функцию.</span><span class="sxs-lookup"><span data-stu-id="4e44a-119">Schannel returns a token to the server, and a return code indicating whether the server must call the function again.</span></span>
3.  <span data-ttu-id="4e44a-120">Если маркер был возвращен, сервер отправляет его клиенту.</span><span class="sxs-lookup"><span data-stu-id="4e44a-120">If a token was returned, the server sends it to the client.</span></span>
4.  <span data-ttu-id="4e44a-121">Когда [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) возвращает значение \_ \_ в секунду, то сервер выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e44a-121">When [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) returns SEC\_E\_OK, the server is done.</span></span> <span data-ttu-id="4e44a-122">Если функция возвращает секунды \_ , то \_ \_ сервер должен подождать, пока клиент отправит ему маркер.</span><span class="sxs-lookup"><span data-stu-id="4e44a-122">If the function returns SEC\_I\_CONTINUE\_NEEDED, then the server must wait for the client to send it a token.</span></span> <span data-ttu-id="4e44a-123">Если сервер имеет маркер от клиента, он должен снова вызвать функцию **AcceptSecurityContext (General)** .</span><span class="sxs-lookup"><span data-stu-id="4e44a-123">When the server has the token from the client, it must call the **AcceptSecurityContext (General)** function again.</span></span> <span data-ttu-id="4e44a-124">(Вернитесь к шагу 2.)</span><span class="sxs-lookup"><span data-stu-id="4e44a-124">(Return to step 2.)</span></span>

<span data-ttu-id="4e44a-125">Если любая из функций возвращает значение, отличное от \_ \_ "в секунду", в секундах по мере \_ \_ \_ необходимости, или с \_ \_ неполным \_ сообщением (см. следующий абзац), произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4e44a-125">If either function returns a value other than SEC\_E\_OK, SEC\_I\_CONTINUE\_NEEDED, or SEC\_E\_INCOMPLETE\_MESSAGE (see the following paragraph) an error has occurred.</span></span> <span data-ttu-id="4e44a-126">Клиент и сервер должны вызвать функцию [**делетесекуритиконтекст**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) для удаления частично установленного контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="4e44a-126">The client and server should call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function to delete the partially established security context.</span></span>

<span data-ttu-id="4e44a-127">Особый случай, который может изменить обработку на стороне клиента и сервера, заключается в том, что на клиент или сервер с другой стороны отправляется слишком мало или слишком много информации.</span><span class="sxs-lookup"><span data-stu-id="4e44a-127">A special case that can alter client and server processing is when too little or too much information is sent to the client or server from the other party.</span></span> <span data-ttu-id="4e44a-128">В случае слишком небольшого объема информации обе функции возвращают \_ сообщение с \_ неполным указанием «е» \_ .</span><span class="sxs-lookup"><span data-stu-id="4e44a-128">In the case of too little information, both functions return SEC\_E\_INCOMPLETE\_MESSAGE.</span></span> <span data-ttu-id="4e44a-129">Сведения об распознавании и обработке недостаточных или избыточных сведений см. [в разделе дополнительные буферы, возвращаемые SChannel](extra-buffers-returned-by-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="4e44a-129">For information about recognizing and handling insufficient or excess information, see [Extra buffers Returned by Schannel](extra-buffers-returned-by-schannel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e44a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4e44a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e44a-131">Выполнение проверки подлинности с помощью канала Schannel</span><span class="sxs-lookup"><span data-stu-id="4e44a-131">Performing Authentication Using Schannel</span></span>](performing-authentication-using-schannel.md)
</dt> <dt>

[<span data-ttu-id="4e44a-132">Сопоставление сертификатов</span><span class="sxs-lookup"><span data-stu-id="4e44a-132">Mapping Certificates</span></span>](mapping-certificates.md)
</dt> <dt>

[<span data-ttu-id="4e44a-133">Проверка учетных данных SChannel вручную</span><span class="sxs-lookup"><span data-stu-id="4e44a-133">Manually Validating Schannel Credentials</span></span>](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 

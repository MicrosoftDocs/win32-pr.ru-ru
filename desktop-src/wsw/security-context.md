---
title: Контекст безопасности
description: Контексты безопасности обеспечивают возможность установки контекста безопасности сообщений в соответствии с WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Собственный контекст безопасности — веб-службы
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339677"
---
# <a name="security-context"></a><span data-ttu-id="761dd-106">Контекст безопасности</span><span class="sxs-lookup"><span data-stu-id="761dd-106">Security Context</span></span>

<span data-ttu-id="761dd-107">Контексты безопасности обеспечивают возможность установки контекста безопасности сообщений в соответствии с WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="761dd-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="761dd-108">Этот контекст затем можно использовать для защиты сообщений в качестве альтернативы безопасности для одного снимка, при которой учетные данные передаются для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="761dd-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="761dd-109">Установленный контекст безопасности является более эффективным способом защиты сообщений при обмене данными между несколькими сообщениями.</span><span class="sxs-lookup"><span data-stu-id="761dd-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="761dd-110">Контекст безопасности требует наличия учетных данных безопасности начальной загрузки, которые используются для защиты сообщений, отправляемых в контексте.</span><span class="sxs-lookup"><span data-stu-id="761dd-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="761dd-111">Для этой цели можно использовать привязку безопасности [**\_ сообщений WS Kerberos \_ апрек \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**\_ \_ \_ \_ \_ привязку безопасности сообщений WS XML Token**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), а также структуры [**\_ \_ \_ \_ привязки безопасности сообщений имени пользователя**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) .</span><span class="sxs-lookup"><span data-stu-id="761dd-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="761dd-112">Контексты безопасности — это функция безопасности сообщений, настроенная с помощью привязок безопасности сообщений.</span><span class="sxs-lookup"><span data-stu-id="761dd-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="761dd-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="761dd-113">Client</span></span>

<span data-ttu-id="761dd-114">На стороне клиента контекст безопасности привязан к определенному каналу.</span><span class="sxs-lookup"><span data-stu-id="761dd-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="761dd-115">Он настраивается с [**помощью \_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span><span class="sxs-lookup"><span data-stu-id="761dd-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="761dd-116">Поведение и время существования контекста определяются каналом.</span><span class="sxs-lookup"><span data-stu-id="761dd-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="761dd-117">При отправке первого сообщения по каналу устанавливается контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="761dd-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="761dd-118">После этого контекст будет заблаговременно обновляться с настраиваемым интервалом.</span><span class="sxs-lookup"><span data-stu-id="761dd-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="761dd-119">Если сервер возвращает ошибку, указывающую на необходимость продления контекста, контекст обновляется при отправке следующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="761dd-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="761dd-120">Если канал находится в открытом состоянии, контекст отменяется сообщением об отмене при закрытии канала.</span><span class="sxs-lookup"><span data-stu-id="761dd-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="761dd-121">Сервер</span><span class="sxs-lookup"><span data-stu-id="761dd-121">Server</span></span>

<span data-ttu-id="761dd-122">На сервере контекст безопасности настраивается так же, как и на клиенте.</span><span class="sxs-lookup"><span data-stu-id="761dd-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="761dd-123">Однако он не привязан к какому-либо конкретному каналу.</span><span class="sxs-lookup"><span data-stu-id="761dd-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="761dd-124">Вместо этого все каналы, созданные для прослушивателя с набором [**\_ \_ \_ \_ \_ привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) , могут получать сообщения с любыми контекстами безопасности, установленными на каналах этого прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="761dd-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="761dd-125">При поступлении сообщения в канал, поддерживающий контекст безопасности, контекст, используемый этим сообщением, можно получить, вызвав функцию [**всжетмессажепроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) с [**\_ \_ \_ \_ контекстом безопасности свойства сообщения WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="761dd-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="761dd-126">Извлеченное значение можно использовать с [**всревокесекуритиконтекст**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) и [**всжетсекуритиконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span><span class="sxs-lookup"><span data-stu-id="761dd-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="761dd-127">Метаданные</span><span class="sxs-lookup"><span data-stu-id="761dd-127">Metadata</span></span>

<span data-ttu-id="761dd-128">Структура [**\_ \_ \_ \_ \_ \_ ограничения привязки безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) используется для извлечения политики контекста безопасности из метаданных.</span><span class="sxs-lookup"><span data-stu-id="761dd-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="761dd-129">Дополнительные сведения см. в разделе [Импорт метаданных](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="761dd-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="761dd-130">С контекстами безопасности используются следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="761dd-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="761dd-131">Перечисление</span><span class="sxs-lookup"><span data-stu-id="761dd-131">Enumeration</span></span>                                                                    | <span data-ttu-id="761dd-132">Описание</span><span class="sxs-lookup"><span data-stu-id="761dd-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="761dd-133">**\_ \_ \_ идентификатор свойства контекста безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="761dd-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="761dd-134">Определяет свойство объекта контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="761dd-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="761dd-135">Функция</span><span class="sxs-lookup"><span data-stu-id="761dd-135">Function</span></span>                                                             | <span data-ttu-id="761dd-136">Описание</span><span class="sxs-lookup"><span data-stu-id="761dd-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="761dd-137">**всжетсекуритиконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="761dd-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="761dd-138">Возвращает свойство указанного контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="761dd-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="761dd-139">**всревокесекуритиконтекст**</span><span class="sxs-lookup"><span data-stu-id="761dd-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="761dd-140">Отменяет контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="761dd-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="761dd-141">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="761dd-141">Handle</span></span>                                           | <span data-ttu-id="761dd-142">Описание</span><span class="sxs-lookup"><span data-stu-id="761dd-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="761dd-143">\_контекст безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="761dd-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="761dd-144">Непрозрачный тип, используемый для ссылки на объект контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="761dd-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="761dd-145">Структура</span><span class="sxs-lookup"><span data-stu-id="761dd-145">Structure</span></span>                                                               | <span data-ttu-id="761dd-146">Описание</span><span class="sxs-lookup"><span data-stu-id="761dd-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="761dd-147">**\_ \_ свойство контекста безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="761dd-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="761dd-148">Определяет свойство [ \_ \_ контекста безопасности WS](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="761dd-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 





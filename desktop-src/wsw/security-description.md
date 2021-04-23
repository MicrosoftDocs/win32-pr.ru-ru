---
title: Описание безопасности
description: Описание безопасности представляется \_ \_ структурой описания безопасности WS, а экземпляр описания безопасности предоставляется при вызове функции вскреатечаннел для создания безопасного канала или функции вскреателистенер для создания прослушивателя.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Описание безопасности веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104156979"
---
# <a name="security-description"></a><span data-ttu-id="65486-106">Описание безопасности</span><span class="sxs-lookup"><span data-stu-id="65486-106">Security Description</span></span>

<span data-ttu-id="65486-107">Описание безопасности представляется структурой [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , а экземпляр описания безопасности предоставляется при вызове функции [**вскреатечаннел**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) для создания безопасного канала или функции [**вскреателистенер**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) для создания прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="65486-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="65486-108">Структура описания безопасности</span><span class="sxs-lookup"><span data-stu-id="65486-108">Structure of a Security Description</span></span>

<span data-ttu-id="65486-109">Основная модель обеспечения безопасности канала заключается в том, что канал защищен одним или несколькими маркерами безопасности.</span><span class="sxs-lookup"><span data-stu-id="65486-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="65486-110">В соответствии с этой моделью структура [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) содержит список привязок безопасности, представленных структурами [**\_ \_ привязки безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , и каждая привязка безопасности описывает получение и использование одного маркера безопасности в канале.</span><span class="sxs-lookup"><span data-stu-id="65486-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="65486-111">Тип безопасности, используемый в канале, определяется выбором подтипов привязки безопасности, включенных в описание безопасности.</span><span class="sxs-lookup"><span data-stu-id="65486-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="65486-112">Дополнительные параметры безопасности, относящиеся к привязке безопасности, задаются в виде [параметров привязки](security-binding-settings.md) безопасности в структуре привязки безопасности. Однако параметры на уровне канала, независимые от привязок безопасности, указываются непосредственно в качестве [параметров канала безопасности](security-channel-settings.md) в поле **свойства** самого описания безопасности.</span><span class="sxs-lookup"><span data-stu-id="65486-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![Схема, показывающая структуру описания безопасности.](images/securitydescription.png)

<span data-ttu-id="65486-114">В описаниях безопасности используются следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="65486-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="65486-115">Структура</span><span class="sxs-lookup"><span data-stu-id="65486-115">Structure</span></span>                                                    | <span data-ttu-id="65486-116">Описание</span><span class="sxs-lookup"><span data-stu-id="65486-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65486-117">**\_Описание безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="65486-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="65486-118">Структура верхнего уровня, используемая для указания требований безопасности для канала (на стороне клиента) или прослушивателя (на стороне сервера).</span><span class="sxs-lookup"><span data-stu-id="65486-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 





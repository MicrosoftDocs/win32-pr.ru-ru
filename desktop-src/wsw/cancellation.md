---
title: Отмена
description: Большинство операций в ВВСАПИ могут быть отменены во время выполнения.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Отмена веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339757"
---
# <a name="cancellation"></a><span data-ttu-id="6d006-106">Отмена</span><span class="sxs-lookup"><span data-stu-id="6d006-106">Cancellation</span></span>

<span data-ttu-id="6d006-107">Большинство операций в ВВСАПИ могут быть отменены во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d006-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="6d006-108">Какая функция, используемая для отмены операции, зависит от затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="6d006-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="6d006-109">Функция</span><span class="sxs-lookup"><span data-stu-id="6d006-109">Function</span></span>                                           | <span data-ttu-id="6d006-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6d006-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d006-111">**всабортчаннел**</span><span class="sxs-lookup"><span data-stu-id="6d006-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="6d006-112">Отменяет все ожидающие входные и выходные данные в указанном канале и устанавливает состояние канала в состояние WS \_ канала с \_ \_ ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6d006-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="6d006-113">**всабортлистенер**</span><span class="sxs-lookup"><span data-stu-id="6d006-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="6d006-114">Отменяет все ожидающие входные и выходные данные для указанного прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="6d006-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="6d006-115">**всабортсервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="6d006-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="6d006-116">Отменяет все ожидающие входные и выходные данные для указанного прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="6d006-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="6d006-117">**всабортсервицехост**</span><span class="sxs-lookup"><span data-stu-id="6d006-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="6d006-118">Прерывает и прекращает выполнение текущих операций на узле службы.</span><span class="sxs-lookup"><span data-stu-id="6d006-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="6d006-119">**всабандонкалл**</span><span class="sxs-lookup"><span data-stu-id="6d006-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="6d006-120">Отменяет вызов, указанный вызов для указанного прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="6d006-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="6d006-121">Сведения об отменах, влияющих на [операции службы на стороне сервера](server-side-service-operations.md) и обратные вызовы модели служб, см. в разделе [Отмена вызова](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="6d006-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 





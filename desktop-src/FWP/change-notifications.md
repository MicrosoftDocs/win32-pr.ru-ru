---
title: Уведомления об изменениях
description: Уведомления об изменениях модуля базовой фильтрации (BFE) следуют шаблону публикации/подписки.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987215"
---
# <a name="change-notifications"></a><span data-ttu-id="f2b1a-103">Уведомления об изменениях</span><span class="sxs-lookup"><span data-stu-id="f2b1a-103">Change Notifications</span></span>

<span data-ttu-id="f2b1a-104">Уведомления об изменениях модуля базовой фильтрации (BFE) следуют шаблону публикации или подписки: для получения одного из опубликованных уведомлений об изменениях приложение должно подписаться на него.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="f2b1a-105">Опубликованные уведомления об изменениях BFE добавляются и удаляются для [**вызовов**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**фильтров**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**поставщиков**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**контекстов поставщиков**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)и [**подслоев**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span><span class="sxs-lookup"><span data-stu-id="f2b1a-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="f2b1a-106">Чтобы подписываться на одно из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления [**фвпм \* SubscribeChanges0**](fwp-mgmt-functions.md) (например, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="f2b1a-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="f2b1a-107">Функция обратного вызова, передаваемая в качестве аргумента в **фвпм \* SubscribeChanges0** , вызывается BFE при возникновении изменения, на которое она подписана.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="f2b1a-108">Чтобы отказаться от подписки на одно из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления **фвпм \* UnsubscribeChanges0** (например, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="f2b1a-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="f2b1a-109">Чтобы просмотреть текущие подписки для одного из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления [**фвпм \* SubscriptionsGet0**](fwp-mgmt-functions.md) (например, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="f2b1a-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="f2b1a-110">Уведомления об изменениях, предлагаемые BFE:</span><span class="sxs-lookup"><span data-stu-id="f2b1a-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="f2b1a-111">Асинхронно — вызов функции, который активировал уведомление, может вернуть, прежде чем уведомление будет отправлено всем подписчикам.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="f2b1a-112">Ненадежные — не гарантируется, что уведомления будут успешно доставлены.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="f2b1a-113">Подписчики не получают уведомления об изменениях, внесенных в обработчик сеанса, который они использовали для подписки.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="f2b1a-114">Как правило, подписчики должны информироваться только об изменениях, внесенных другими пользователями; они уже узнают, какие изменения были внесены самим собой.</span><span class="sxs-lookup"><span data-stu-id="f2b1a-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 





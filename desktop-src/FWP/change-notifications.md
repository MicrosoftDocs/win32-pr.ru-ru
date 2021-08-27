---
title: Уведомления об изменениях
description: Уведомления об изменениях модуля базовой фильтрации (BFE) следуют шаблону публикации/подписки.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0038dc851cb15414dbc0180f205104725bf069b599632a93ae6e257fe7a1f84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078504"
---
# <a name="change-notifications"></a>Уведомления об изменениях

Уведомления об изменениях модуля базовой фильтрации (BFE) следуют шаблону публикации или подписки: для получения одного из опубликованных уведомлений об изменениях приложение должно подписаться на него.

Опубликованные уведомления об изменениях BFE добавляются и удаляются для [**вызовов**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**фильтров**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**поставщиков**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**контекстов поставщиков**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)и [**подслоев**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).

Чтобы подписываться на одно из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления [**фвпм \* SubscribeChanges0**](fwp-mgmt-functions.md) (например, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). Функция обратного вызова, передаваемая в качестве аргумента в **фвпм \* SubscribeChanges0** , вызывается BFE при возникновении изменения, на которое она подписана.

Чтобы отказаться от подписки на одно из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления **фвпм \* UnsubscribeChanges0** (например, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Чтобы просмотреть текущие подписки для одного из перечисленных выше уведомлений, приложение вызывает соответствующую функцию управления [**фвпм \* SubscriptionsGet0**](fwp-mgmt-functions.md) (например, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

Уведомления об изменениях, предлагаемые BFE:

-   Асинхронно — вызов функции, который активировал уведомление, может вернуть, прежде чем уведомление будет отправлено всем подписчикам.
-   Ненадежные — не гарантируется, что уведомления будут успешно доставлены.

Подписчики не получают уведомления об изменениях, внесенных в обработчик сеанса, который они использовали для подписки. Как правило, подписчики должны информироваться только об изменениях, внесенных другими пользователями; они уже узнают, какие изменения были внесены самим собой.

 

 





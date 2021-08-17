---
description: Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Получение уведомлений о сетевых событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146617"
---
# <a name="receiving-notification-of-network-events"></a>Получение уведомлений о сетевых событиях

Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.

Используйте функцию [**нотифяддрчанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) для запроса уведомления об изменениях, происходящих в сопоставлении между IP-адресами и интерфейсами на локальном компьютере.

Аналогичным образом функция [**нотифираутечанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) позволяет приложению запрашивать уведомления о любых изменениях, происходящих в таблице маршрутизации IP.

Уведомления, предоставляемые этими функциями, не указывают, что изменилось; они просто указывают, что что-то изменилось. Используйте другие вспомогательные функции IP, такие как [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) и [**жетбестрауте**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), чтобы определить точную природу изменения.

 

 




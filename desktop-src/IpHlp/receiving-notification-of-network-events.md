---
description: Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Получение уведомлений о сетевых событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682613"
---
# <a name="receiving-notification-of-network-events"></a>Получение уведомлений о сетевых событиях

Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.

Используйте функцию [**нотифяддрчанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) для запроса уведомления об изменениях, происходящих в сопоставлении между IP-адресами и интерфейсами на локальном компьютере.

Аналогичным образом функция [**нотифираутечанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) позволяет приложению запрашивать уведомления о любых изменениях, происходящих в таблице маршрутизации IP.

Уведомления, предоставляемые этими функциями, не указывают, что изменилось; они просто указывают, что что-то изменилось. Используйте другие вспомогательные функции IP, такие как [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) и [**жетбестрауте**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), чтобы определить точную природу изменения.

 

 




---
description: Windows Элементы интерфейса Sockets 2 (Winsock) для MultiPoint и многоадресной рассылки.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Сокеты 2. элементы интерфейса для MultiPoint и многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf2422d8171a041f75ba8abed6ea490982187af3affb3d3c3d1349984210ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558856"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Сокеты 2. элементы интерфейса для MultiPoint и многоадресной рассылки

механизмы, включенные в Windows сокеты 2 для использования возможностей multipoint, можно суммировать следующим образом.

-   Три бита атрибутов в структуре [**\_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Четыре флага, определенные  для параметра dwFlags [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Одна функция [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)для добавления конечных узлов в сеанс MultiPoint.
-   Два кода команд [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) для управления замыканием на себя MultiPoint и областью многоадресных передач.

В следующих разделах эти элементы интерфейса описаны более подробно:

-   [Семантика присоединения к листьям MultiPoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Как существующие протоколы MultiPoint поддерживают эти расширения](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 

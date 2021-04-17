---
description: Элементы интерфейса Windows Sockets 2 (Winsock) для MultiPoint и многоадресной рассылки.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Элементы интерфейса сокетов Windows 2 для MultiPoint и многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711379"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Элементы интерфейса сокетов Windows 2 для MultiPoint и многоадресной рассылки

Механизмы, включенные в сокеты Windows 2 для использования возможностей MultiPoint, можно суммировать следующим образом.

-   Три бита атрибутов в структуре [**\_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Четыре флага, определенные  для параметра dwFlags [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Одна функция [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)для добавления конечных узлов в сеанс MultiPoint.
-   Два кода команд [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) для управления замыканием на себя MultiPoint и областью многоадресных передач.

В следующих разделах эти элементы интерфейса описаны более подробно:

-   [Семантика присоединения к листьям MultiPoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Как существующие протоколы MultiPoint поддерживают эти расширения](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 

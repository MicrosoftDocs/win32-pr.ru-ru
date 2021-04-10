---
description: Функция сокета создала сокеты с атрибутом OVERLAPPED, установленным по умолчанию в первой Wsock32.dll, 32-разрядной версии сокетов Windows (1,1).
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Состояние по умолчанию для перекрывающихся атрибутов сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145082"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Состояние по умолчанию для перекрывающихся атрибутов сокета

Функция [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) создала сокеты с атрибутом OVERLAPPED, установленным по умолчанию в первой Wsock32.dll, 32-разрядной версии сокетов Windows (1,1). Чтобы обеспечить обратную совместимость с развернутыми реализациями Wsock32.dll, это будет продолжаться и для сокетов Windows 2. То есть, в сокетах Windows Sockets 2, созданных с помощью функции **сокета** , будет иметь атрибут OVERLAPPED. Однако, чтобы быть более совместимым с остальной частью API Windows, сокеты, созданные с помощью [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , по умолчанию не будут иметь атрибут OVERLAPPED. Этот атрибут будет применен только в том случае, \_ Если \_ установлен бит с перекрытием флага WSA.

 

 




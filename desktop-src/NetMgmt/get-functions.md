---
title: Получение функций
description: Функции сетевого управления Get получают сведения о домене. Эти функции также можно вызывать для получения сведений о локальных, глобальных, рабочих станциях и учетных записях пользователя сервера.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532237"
---
# <a name="get-functions"></a>Получение функций

Функции сетевого управления Get получают сведения о домене. Эти функции также можно вызывать для получения сведений о локальных, глобальных, рабочих станциях и учетных записях пользователя сервера.

Ниже перечислены функции Get для управления сетью.



| Функция                                                               | Описание                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетжетанидкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Возвращает имя любого контроллера домена для домена, который напрямую является доверенным для указанного сервера.                                   |
| [**нетжетдкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Возвращает имя основного контроллера домена (PDC) для указанного домена.                                                        |
| [**нетжетдисплайинформатиониндекс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Возвращает индекс первой записи отображаемой информации, имя которой начинается с указанной строки или в алфавитном порядке за строкой. |
| [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Возвращает сведения об учетной записи пользователя, компьютера или глобальной группы.                                                                             |



 

Сведения, возвращаемые функцией [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) , доступны на следующих уровнях:

-   [**\_Группа дисплеев NET \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**NET \_ диспле \_ компьютера**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**\_пользователь NET дисплея \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 





---
title: Обмен данными между клиентом и сервером
description: Механизм Виневентс предоставляет серверам возможность легко обмениваться данными с клиентами Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133937"
---
# <a name="clientserver-communication"></a>Обмен данными между клиентом и сервером

Механизм [виневентс](winevents-overview.md) предоставляет серверам возможность легко обмениваться данными с клиентами Microsoft Active Accessibility. Клиенты часто собираются данные путем реагирования на Виневентс (например, следующий фокус), но они могут запрашивать информацию с сервера в любое время.

Чтобы запросить сведения для объекта со специальными возможностями, создающего WinEvent, клиент должен обработать событие и установить соединение с соответствующим доступным объектом. Для этого клиент выполняет следующие шесть шагов:

-   Сервер вызывает [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , чтобы создать уведомление WinEvent для каждого изменения в своих элементах пользовательского интерфейса.
-   Код управления WinEvent в USER определяет, зарегистрировал ли клиентские приложения [*функцию-обработчик*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent с помощью [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) и вызывает зарегистрированную функцию обратного вызова.
-   В функции обратного вызова клиент запрашивает доступ к объекту, создавшему событие, путем вызова [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) или других функций получения доступных объектов. Дополнительные сведения см. в разделе [Получение объекта IAccessible](retrieving-an-iaccessible-object.md).
-   Этот API Microsoft Active Accessibility отправляет серверное приложение сообщение [**WM \_ GetObject**](wm-getobject.md) для получения доступного объекта.
-   В ответ на функцию [**WM \_ GetObject**](wm-getobject.md)серверное приложение возвращает либо ноль, либо возвращает значение, которое выступает в качестве одноразовой ссылки на объект, создавший событие.
-   Если сервер возвращает значение 0, Microsoft Active Accessibility создает прокси-объект и предоставляет клиенту свой адрес. В противном случае Microsoft Active Accessibility использует эту ссылку для получения адреса объектного интерфейса, такого как [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) или [**IDispatch**](idispatch-interface.md), и предоставляет клиенту этот адрес.

После того как у клиента есть адрес интерфейса, он может вызывать свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и методы доступного объекта для получения информации.

## <a name="in-this-section"></a>Содержание раздела

-   [Виневентс и Active Accessibility](winevents-overview.md)
-   [Как \_ работает WM GetObject](how-wm-getobject-works.md)
-   [Получение объекта IAccessible](retrieving-an-iaccessible-object.md)

 

 





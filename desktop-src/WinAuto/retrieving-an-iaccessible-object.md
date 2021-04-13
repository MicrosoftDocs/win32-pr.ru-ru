---
title: Получение объекта IAccessible
description: Microsoft Active Accessibility предоставляет такие функции, как Акцессиблеобжектфромвиндов и Акцессиблеобжектфромпоинт, которые позволяют клиентам получать доступные объекты.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328792"
---
# <a name="retrieving-an-iaccessible-object"></a>Получение объекта IAccessible

Microsoft Active Accessibility предоставляет такие функции, как [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) , которые позволяют клиентам получать доступные объекты. Эти функции возвращают указатель на интерфейс [**IDispatch**](idispatch-interface.md) или [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , через который клиенты получают сведения о доступном объекте.

Когда клиент вызывает [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) или любую другую функцию **акцессиблеобжектфром * * * X* , которая получает интерфейс к объекту, Microsoft Active Accessibility отправляет сообщение в окне [**WM \_ GetObject**](wm-getobject.md) в соответствующую процедуру в соответствующем приложении. Чтобы предоставить сведения клиентам, серверы должны отвечать на сообщение **WM \_ GetObject** .

Чтобы получить конкретные сведения об элементе пользовательского интерфейса, клиенты должны сначала получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента. Чтобы получить объект **IAccessible** элемента, клиенты могут использовать одну из следующих функций:

-   [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Получение указателя на интерфейс IAccessible**

1.  Клиент вызывает одну из функций **акцессиблеобжектфром * * * X* .
2.  Oleacc.dll отправляет сообщение [**WM \_ GetObject**](wm-getobject.md) на сервер.
3.  Сервер определяет, какой элемент пользовательского интерфейса соответствует запросу.
4.  Сервер либо возвращает нуль, чтобы запросить Oleacc.dll прокси-сервер,

    либо

    Возвращает объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (собственная реализация). Для этого выполните следующие действия.

    -   Конструирует объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента.
    -   Вызывает [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) для маршалирования указателя объекта.
    -   Возвращает LRESULT для Oleacc.dll.

5.  Oleacc.dll проверяет возвращаемое значение из [**WM \_ GetObject**](wm-getobject.md).

    Если он равен нулю, Oleacc.dll конструирует прокси-объект и возвращает его клиенту.

    либо

    Если значение не равно нулю, Oleacc.dll вызывает метод [**обжектфромлресулт**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) для распаковки указателя на собственный объект [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и возвращает его клиенту.

 

 





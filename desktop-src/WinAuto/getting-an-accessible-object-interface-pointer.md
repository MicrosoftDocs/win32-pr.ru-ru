---
title: Получение указателя на интерфейсный объект с доступом
description: Клиентские приложения Microsoft Active Accessibility получают указатели интерфейсов на доступные объекты с помощью одной из следующих функций.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994204"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Получение указателя на интерфейсный объект с доступом

Клиентские приложения Microsoft Active Accessibility получают указатели интерфейсов на доступные объекты с помощью одной из следующих функций.

**акцессиблеобжектфромевент**

Многие клиенты ищут сведения о конкретных специальных объектах, создающих события. Поскольку интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) является "шлюзом" к доступным объектам, клиенты должны иметь простой способ связать [виневентс](winevents-overview.md) с интерфейсом **IAccessible** объекта, создающего события. Microsoft Active Accessibility предоставляет функцию [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) специально для этой цели.

> [!Note]  
> Клиенты с [функциями-обработчиками в контексте](in-context-hook-functions.md) должны вызывать функцию « [Window»](/windows/win32/api/winuser/nf-winuser-iswindow) перед вызовом [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

Функция [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) принимает большую часть той же информации, которую получает клиентский [*функция-ловушка*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) . Когда функция-обработчик клиента получает уведомление о событии, она передает соответствующие параметры из событий в **акцессиблеобжектфромевент**.

Функция получает либо интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) элемента пользовательского интерфейса, создавшего событие, либо интерфейс родительского объекта элемента. Если возвращается указатель интерфейса родительского объекта, клиент вызывает свойства и методы родителя, чтобы получить сведения о дочернем элементе, создавшем событие.

**акцессиблеобжектфромпоинт**

Чтобы получить адрес интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта в заданной точке экрана, клиенты используют функцию [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) .

**акцессиблеобжектфромвиндов**

Чтобы получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта из маркера окна, клиенты используют функцию [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

Возможно, что серверы возвращают разные указатели интерфейса для одного и того же элемента пользовательского интерфейса каждый раз, когда вызывается функция [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)или [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . Чтобы определить, ссылаются ли два указателя на один и тот же элемент пользовательского интерфейса, клиентские разработчики должны сравнить свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта, а не указатели.

 

 
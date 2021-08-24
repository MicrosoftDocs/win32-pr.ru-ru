---
title: Как работает WM_GETOBJECT
description: Microsoft Active Accessibility отправляет сообщение WM \_ GetObject в соответствующее серверное приложение, когда клиент вызывает одну из функций акцессиблеобжектфромкс.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795764"
---
# <a name="how-wm_getobject-works"></a>Как \_ работает WM GetObject

Microsoft Active Accessibility отправляет сообщение [**WM \_ GetObject**](wm-getobject.md) в соответствующее серверное приложение, когда клиент вызывает одну из функций **акцессиблеобжектфром**_X_ . В следующем списке описаны различные сценарии, которые происходят:

-   Если окно или элемент управления, принимающий [**WM \_ GetObject**](wm-getobject.md) , реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), то окно возвращает ссылку на интерфейс **IAccessible** с помощью [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, в сочетании с библиотекой модели COM, выполняет соответствующий маршалирование и передает указатель интерфейса с сервера обратно клиенту.
-   Если окно, принимающее сообщение, не реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), оно должно вернуть ноль.
-   Если окно не обрабатывает сообщение [**WM \_ GetObject**](wm-getobject.md) , функция [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) возвращает ноль.

Даже если сервер возвращает значение 0, Microsoft Active Accessibility по-прежнему предоставляет клиенту сведения об объекте. Для большинства предоставляемых системой объектов, таких как списки и кнопки, Microsoft Active Accessibility предоставляет полную информацию. для других объектов сведения ограничены. Например, Microsoft Active Accessibility не предоставляет сведения для элементов управления, которые не имеют обработчика окна. Microsoft Active Accessibility возвращает указатель на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) прокси-сервера, используемый клиентом для получения сведений об объекте.

Дополнительные сведения см. [в описании \_ сообщения WM GetObject](the-wm-getobject-message.md).

 

 
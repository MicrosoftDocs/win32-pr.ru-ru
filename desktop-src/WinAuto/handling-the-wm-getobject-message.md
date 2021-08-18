---
title: Обработка сообщения WM_GETOBJECT
description: Как Microsoft Active Accessibility, так и Microsoft UI Automation отправляют \_ сообщение WM GetObject серверу или приложению поставщика для получения сведений о доступном объекте, поддерживаемом сервером или поставщиком.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732ebd21cc6d198040e5502554ce2a8cf1abb718c055bc9af9f88e0c5d123b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994194"
---
# <a name="handling-the-wm_getobject-message"></a>Обработка сообщения WM \_ GetObject

Как Microsoft Active Accessibility, так и Microsoft UI Automation отправляют сообщение [**WM \_ GetObject**](wm-getobject.md) серверу или приложению поставщика для получения сведений о доступном объекте, поддерживаемом сервером или поставщиком. Клиенты никогда не отправляют **WM \_ GetObject** напрямую. Вместо этого, Microsoft Active Accessibility отправляет это сообщение, когда клиент вызывает функции [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)и [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . Автоматизация пользовательского интерфейса **отправляет \_ объект WM GetObject** , когда клиент [**вызывает иуиаутоматион:: Елементфромхандле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)и [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), а также при обработке событий, для которых зарегистрирован клиент.

Microsoft Active Accessibility или модель автоматизации пользовательского интерфейса определяет тип объекта, для которого требуются сведения, передавая значение, называемое *идентификатором объекта* , с сообщением [**WM \_ GetObject**](wm-getobject.md) . При получении сообщения сервер или поставщик проверяет идентификатор объекта, чтобы определить, как реагировать на сообщение. Ответ зависит от того, реализует ли принимающее приложение Microsoft Active Accessibility (сервер), автоматизацию пользовательского интерфейса (поставщика) или ни один из них для указанного объекта.

-   Если принимающее приложение является сервером Microsoft Active Accessibility, а сообщение [**WM \_ GetObject**](wm-getobject.md) содержит идентификатор объекта [**\_ клиента OBJID**](object-identifiers.md), сервер должен вернуть значение, полученное путем передачи интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта в функцию [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Если принимающее приложение является поставщиком автоматизации АУИ и идентификатором объекта является **уиарутобжектид**, поставщик должен вернуть интерфейс [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) объекта. Поставщик получает интерфейс путем вызова функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Если принимающее приложение не реализует ни Microsoft Active Accessibility, ни автоматизацию пользовательского интерфейса, оно должно передать сообщение [**WM \_ GetObject**](wm-getobject.md) функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Передача сообщения позволяет платформе специальных возможностей определить, доступен ли прокси-сервер для указанного объекта.
-   Если идентификатор объекта не является ни [**OBJID \_ клиентом**](object-identifiers.md) , ни уиарутобжектид, принимающее приложение должно передать сообщение [**WM \_ GetObject**](wm-getobject.md) функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Передача сообщения позволяет платформе специальных возможностей использовать поставщики по умолчанию для стандартных элементов пользовательского интерфейса.

Microsoft Active Accessibility и служба автоматизации пользовательского интерфейса могут передавать идентификаторы пользовательских объектов в сообщении [**WM \_ GetObject**](wm-getobject.md) для получения определяемых приложением значений или объектов с сервера или поставщика. Идентификатор объекта [**OBJID \_ Нативеом**](object-identifiers.md) или [**OBJID \_ куерикласснамеидкс**](object-identifiers.md) можно использовать для получения интерфейса собственной объектной модели или для запроса определенного прокси-объекта, поддерживаемого Oleacc.dll.

При обработке идентификаторов [**OBJID \_ клиента**](object-identifiers.md) и объекта **уиарутобжектид** реализация сервера Microsoft Active Accessibility Server может сосуществовать наряду с реализацией поставщика автоматизации пользовательского интерфейса. поскольку большинство стандартных элементов управления Windows и общих элементов управления, реализованных в общей библиотеке элементов управления (ComCtl32.dll), не реализуют ни Microsoft Active Accessibility, ни автоматизацию пользовательского интерфейса, эти элементы управления обычно не обрабатывали сообщение [**WM \_ getobject**](wm-getobject.md) . Вместо этого платформа Microsoft Active Accessibility или модель автоматизации пользовательского интерфейса проверяет, доступен ли прокси-объект для определенного элемента пользовательского интерфейса. В противном случае он предоставляет прокси-объект по умолчанию для объекта окна узла.

 

 
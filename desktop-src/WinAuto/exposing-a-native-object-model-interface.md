---
title: Предоставление собственного интерфейса объектной модели
description: Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на \_ сообщения WM GetObject, которые содержат \_ идентификатор объекта нативеом OBJID.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068204"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="93abe-103">Предоставление собственного интерфейса объектной модели</span><span class="sxs-lookup"><span data-stu-id="93abe-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="93abe-104">Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на сообщения [**WM \_ GetObject**](wm-getobject.md) , которые содержат идентификатор объекта [**\_ нативеом OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="93abe-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="93abe-105">Для ответа элемент пользовательского интерфейса должен возвращать значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="93abe-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="93abe-106">Клиент может получить интерфейс из элемента пользовательского интерфейса, поддерживающего собственную объектную модель, вызвав функцию [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и указав [**OBJID \_ нативеом**](object-identifiers.md) в качестве второго параметра.</span><span class="sxs-lookup"><span data-stu-id="93abe-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 





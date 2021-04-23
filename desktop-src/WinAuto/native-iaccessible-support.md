---
title: Собственная поддержка IAccessible
description: Oleacc.dll реализует ИакЦидентити от имени клиента OBJID, \_ а также указатели интерфейсов IAccessible и их непосредственные простые элементы.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888664"
---
# <a name="native-iaccessible-support"></a><span data-ttu-id="0d9d6-103">Собственная поддержка IAccessible</span><span class="sxs-lookup"><span data-stu-id="0d9d6-103">Native IAccessible Support</span></span>

<span data-ttu-id="0d9d6-104">Oleacc.dll реализует [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) от имени [**\_ клиентских**](object-identifiers.md)интерфейсов  [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) OBJID и их немедленные простые элементы.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-104">Oleacc.dll implements [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) on behalf of [**OBJID\_CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers and their immediate simple element children.</span></span> <span data-ttu-id="0d9d6-105">Указатель интерфейса  **IAccessible** **\_ клиента OBJID** возвращается, когда приложение [**WM \_ GetObject**](wm-getobject.md) с *lParam*  =  **OBJID \_** отправляется в **HWND**, которое представляет клиентскую область окна или элемента управления в целом.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-105">An **OBJID\_CLIENT** **IAccessible** interface pointer is returned when [**WM\_GETOBJECT**](wm-getobject.md) with *lParam* = **OBJID\_CLIENT** is sent to an **HWND**, which represents the client area of the window or the control as a whole.</span></span> <span data-ttu-id="0d9d6-106">Родительский объект такого указателя интерфейса **IAccessible** обычно имеет роль [**\_ системного \_ окна роли**](object-roles.md) и является объектом **IAccessible** , возвращаемым при отправке окна **WM \_ GetObject** с *lParam*  =  [**OBJID в \_**](object-identifiers.md) HWND.</span><span class="sxs-lookup"><span data-stu-id="0d9d6-106">The parent of such an **IAccessible** interface pointer will typically have a role of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and is the **IAccessible** object returned when **WM\_GETOBJECT** with *lParam* = [**OBJID\_WINDOW**](object-identifiers.md) is sent to an hwnd.</span></span>

<span data-ttu-id="0d9d6-107">Эти указатели на интерфейсы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) обычно возникают там, где Oleacc.dll прокси-сервер, или когда простой пользовательский элемент управления (например, контейнер **IAccessible** плюс один уровень элементов простого элемента) предоставляет собственную реализацию **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="0d9d6-107">These [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers typically occur where an Oleacc.dll proxy is subclassed, or where a simple custom control (such as a container **IAccessible** plus one level of simple element children) provides a native **IAccessible** implementation.</span></span>

<span data-ttu-id="0d9d6-108">Более сложные собственные реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , такие как место существования иерархии **IAccessible** или идентификаторы пользовательских объектов, должны реализовывать сами [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .</span><span class="sxs-lookup"><span data-stu-id="0d9d6-108">More complicated native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementations such as where a hierarchy of **IAccessible** s exists or where custom object IDs are used must implement [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) themselves.</span></span>

 

 





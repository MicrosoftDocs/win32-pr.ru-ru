---
title: Собственная поддержка IAccessible
description: Oleacc.dll реализует ИакЦидентити от имени клиента OBJID, \_ а также указатели интерфейсов IAccessible и их непосредственные простые элементы.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565058"
---
# <a name="native-iaccessible-support"></a>Собственная поддержка IAccessible

Oleacc.dll реализует [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) от имени [**\_ клиентских**](object-identifiers.md) интерфейсов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) OBJID и их немедленные простые элементы. Указатель интерфейса **IAccessible** **\_ клиента OBJID** возвращается, когда приложение [**WM \_ GetObject**](wm-getobject.md) с *lParam*  =  **OBJID \_** отправляется в **HWND**, которое представляет клиентскую область окна или элемента управления в целом. Родительский объект такого указателя интерфейса **IAccessible** обычно имеет роль [**\_ системного \_ окна роли**](object-roles.md) и является объектом **IAccessible** , возвращаемым при отправке окна **WM \_ GetObject** с *lParam*  =  [**OBJID в \_**](object-identifiers.md) HWND.

Эти указатели на интерфейсы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) обычно возникают там, где Oleacc.dll прокси-сервер, или когда простой пользовательский элемент управления (например, контейнер **IAccessible** плюс один уровень элементов простого элемента) предоставляет собственную реализацию **IAccessible** .

Более сложные собственные реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , такие как место существования иерархии **IAccessible** или идентификаторы пользовательских объектов, должны реализовывать сами [**иакЦидентити**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .

 

 





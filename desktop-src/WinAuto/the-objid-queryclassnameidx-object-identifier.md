---
title: Идентификатор объекта OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility использует \_ идентификатор объекта КУЕРИКЛАССНАМЕИДКС OBJID с \_ сообщением WM GetObject для определения класса, к которому принадлежит стандартный элемент управления Windows или обычный элемент управления.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700483"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>\_Идентификатор объекта КУЕРИКЛАССНАМЕИДКС OBJID

Microsoft Active Accessibility использует идентификатор [**объекта \_ куерикласснамеидкс OBJID**](object-identifiers.md) с сообщением [**WM \_ GetObject**](wm-getobject.md) для определения класса, к которому принадлежит стандартный элемент управления Windows или обычный элемент управления. Элемент управления реагирует на это сообщение, возвращая значение, которое Microsoft Active Accessibility сопоставляется с именем класса элемента управления. Microsoft Active Accessibility использует эти сведения, чтобы обеспечить поддержку специальных возможностей для стандартных элементов управления Windows и общих элементов управления.

Как правило, только стандартные элементы управления Windows и общие элементы управления реагируют на идентификатор объекта [**\_ куерикласснамеидкс OBJID**](object-identifiers.md) . Однако пользовательский элемент управления также может отвечать, если он включает все функции, аналогичные стандартному элементу управления Windows или обычному элементу управления. Это обеспечивает поддержку пользовательского элемента управления одним из стандартных прокси-объектов, предоставляемых Microsoft Active Accessibility.

Дополнительные сведения см. в [приложении F: значения идентификаторов объектов для OBJID \_ куерикласснамеидкс](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 





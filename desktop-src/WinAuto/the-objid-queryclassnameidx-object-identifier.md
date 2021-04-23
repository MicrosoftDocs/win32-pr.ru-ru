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
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="9eb4b-103">\_Идентификатор объекта КУЕРИКЛАССНАМЕИДКС OBJID</span><span class="sxs-lookup"><span data-stu-id="9eb4b-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="9eb4b-104">Microsoft Active Accessibility использует идентификатор [**объекта \_ куерикласснамеидкс OBJID**](object-identifiers.md) с сообщением [**WM \_ GetObject**](wm-getobject.md) для определения класса, к которому принадлежит стандартный элемент управления Windows или обычный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="9eb4b-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="9eb4b-105">Элемент управления реагирует на это сообщение, возвращая значение, которое Microsoft Active Accessibility сопоставляется с именем класса элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9eb4b-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="9eb4b-106">Microsoft Active Accessibility использует эти сведения, чтобы обеспечить поддержку специальных возможностей для стандартных элементов управления Windows и общих элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9eb4b-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="9eb4b-107">Как правило, только стандартные элементы управления Windows и общие элементы управления реагируют на идентификатор объекта [**\_ куерикласснамеидкс OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="9eb4b-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="9eb4b-108">Однако пользовательский элемент управления также может отвечать, если он включает все функции, аналогичные стандартному элементу управления Windows или обычному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="9eb4b-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="9eb4b-109">Это обеспечивает поддержку пользовательского элемента управления одним из стандартных прокси-объектов, предоставляемых Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9eb4b-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="9eb4b-110">Дополнительные сведения см. в [приложении F: значения идентификаторов объектов для OBJID \_ куерикласснамеидкс](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="9eb4b-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 





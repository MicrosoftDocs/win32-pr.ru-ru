---
title: Иерархическая навигация
description: Часто клиенты должны перемещаться между объектами на основе их отношений типа «родители-потомки». Например, клиент может уже иметь сведения об элементе управления ToolBar, но не содержать сведения о кнопках, содержащихся в ней.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253252"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="f0aa9-104">Иерархическая навигация</span><span class="sxs-lookup"><span data-stu-id="f0aa9-104">Hierarchical Navigation</span></span>

<span data-ttu-id="f0aa9-105">Часто клиенты должны перемещаться между объектами на основе их отношений типа «родители-потомки».</span><span class="sxs-lookup"><span data-stu-id="f0aa9-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="f0aa9-106">Например, клиент может уже иметь сведения об элементе управления ToolBar, но не содержать сведения о кнопках, содержащихся в ней.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="f0aa9-107">Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляет иерархические связи между объектами.</span><span class="sxs-lookup"><span data-stu-id="f0aa9-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="f0aa9-108">Клиенты могут переходить от родительского объекта к его дочерним объектам или из дочернего объекта в родительский объект путем вызова метода [**IAccessible:: Get \_ Аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) или [**IAccessible:: Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span><span class="sxs-lookup"><span data-stu-id="f0aa9-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 





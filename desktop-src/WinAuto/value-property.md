---
title: Свойство Value
description: Свойство Value предоставляет текстовое представление визуальных сведений, содержащихся в объекте. Не все объекты поддерживают свойство Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330224"
---
# <a name="value-property"></a><span data-ttu-id="aefbf-104">Свойство Value</span><span class="sxs-lookup"><span data-stu-id="aefbf-104">Value Property</span></span>

<span data-ttu-id="aefbf-105">Свойство **value** предоставляет текстовое представление визуальных сведений, содержащихся в объекте.</span><span class="sxs-lookup"><span data-stu-id="aefbf-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="aefbf-106">Не все объекты поддерживают свойство **value** .</span><span class="sxs-lookup"><span data-stu-id="aefbf-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="aefbf-107">Свойство **value** извлекается путем вызова метода [**IAccessible:: Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="aefbf-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="aefbf-108">Свойство **value** сообщает клиенту о визуальных сведениях, содержащихся в объекте.</span><span class="sxs-lookup"><span data-stu-id="aefbf-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="aefbf-109">Например, значение элемента управления "поле ввода" — это текст, который он содержит, в то время как элемент меню не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="aefbf-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="aefbf-110">Предоставление иерархических сведений</span><span class="sxs-lookup"><span data-stu-id="aefbf-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="aefbf-111">Свойство **value** предоставляет иерархическую информацию в таких случаях, как элемент управления иерархического представления.</span><span class="sxs-lookup"><span data-stu-id="aefbf-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="aefbf-112">Несмотря на то, что родительский объект в элементе управления иерархического представления не предоставляет сведения в свойстве **value** , каждый элемент в элементе управления имеет отсчитываемое от нуля значение, представляющее его уровень в иерархии.</span><span class="sxs-lookup"><span data-stu-id="aefbf-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="aefbf-113">Элементы верхнего уровня имеют нулевое значение, элементы второго уровня имеют значение 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="aefbf-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 





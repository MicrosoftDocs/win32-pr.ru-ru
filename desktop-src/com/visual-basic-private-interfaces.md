---
title: Visual Basic закрытых интерфейсов
description: Visual Basic закрытых интерфейсов
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068620"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="e19a3-103">Visual Basic закрытых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="e19a3-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="e19a3-104">Для категорий компонентов определяются два интерфейса, реализованные Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e19a3-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="e19a3-105">Не ожидается, что элементы управления должны требовать эти категории, поскольку элементы управления могут предлагать альтернативные функции, если они недоступны.</span><span class="sxs-lookup"><span data-stu-id="e19a3-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="e19a3-106">Интерфейс [**ивбформат**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) позволяет элементам управления лучше интегрироваться в среду Visual Basic при форматировании данных.</span><span class="sxs-lookup"><span data-stu-id="e19a3-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="e19a3-107">CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} \_ ВБФОРМАТ CATID</span><span class="sxs-lookup"><span data-stu-id="e19a3-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="e19a3-108">Интерфейс [**ивбжетконтрол**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) позволяет элементу управления перечислять другие элементы управления в форме VB.</span><span class="sxs-lookup"><span data-stu-id="e19a3-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="e19a3-109">CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} \_ ВБЖЕТКОНТРОЛ CATID</span><span class="sxs-lookup"><span data-stu-id="e19a3-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="e19a3-110">Два дополнительных частного интерфейса, [**ижетвбаобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) и [**ижетолеобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), описаны здесь, несмотря на то, что они не определяют категории компонентов.</span><span class="sxs-lookup"><span data-stu-id="e19a3-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="e19a3-111">Использовать эти четыре интерфейса не рекомендуется, так как они не поддерживаются контейнерами, отличными от Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e19a3-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e19a3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e19a3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e19a3-113">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="e19a3-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 





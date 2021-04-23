---
title: елементисчилдофпарентмулиплетимес
description: елементисчилдофпарентмулиплетимес
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259108"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="332e8-103">елементисчилдофпарентмулиплетимес</span><span class="sxs-lookup"><span data-stu-id="332e8-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="332e8-104">Текст</span><span class="sxs-lookup"><span data-stu-id="332e8-104">Text</span></span>

<span data-ttu-id="332e8-105">Аккпарент элемента имеет значение ( {0} ), но исходный элемент — это дочернее {1} время</span><span class="sxs-lookup"><span data-stu-id="332e8-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="332e8-106">Тип</span><span class="sxs-lookup"><span data-stu-id="332e8-106">Type</span></span>

<span data-ttu-id="332e8-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="332e8-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="332e8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="332e8-108">Description</span></span>

<span data-ttu-id="332e8-109">Когда метод [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) вызывается для целевого элемента, он несколько раз передает дочерний элемент того же родителя.</span><span class="sxs-lookup"><span data-stu-id="332e8-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="332e8-110">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="332e8-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="332e8-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="332e8-111">Possible causes</span></span>

<span data-ttu-id="332e8-112">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="332e8-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="332e8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="332e8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="332e8-114">**IAccessible:: Get \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="332e8-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 





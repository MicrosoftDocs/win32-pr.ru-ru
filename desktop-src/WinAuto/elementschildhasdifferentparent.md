---
title: елементсчилдхасдифферентпарент
description: елементсчилдхасдифферентпарент
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332656"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="62fa5-103">елементсчилдхасдифферентпарент</span><span class="sxs-lookup"><span data-stu-id="62fa5-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="62fa5-104">Текст</span><span class="sxs-lookup"><span data-stu-id="62fa5-104">Text</span></span>

<span data-ttu-id="62fa5-105">Дочерний элемент ( {0} ) имеет другой родительский {1} элемент (), чем element</span><span class="sxs-lookup"><span data-stu-id="62fa5-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="62fa5-106">Тип</span><span class="sxs-lookup"><span data-stu-id="62fa5-106">Type</span></span>

<span data-ttu-id="62fa5-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="62fa5-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="62fa5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="62fa5-108">Description</span></span>

<span data-ttu-id="62fa5-109">Эта ошибка означает, что при вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочерних элементов целевого элемента дочерние элементы не сообщают о единообразном родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="62fa5-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![Пример дочерних элементов одного элемента с сообщением о нестабильном родительском элементе](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="62fa5-111">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="62fa5-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="62fa5-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="62fa5-112">Possible causes</span></span>

<span data-ttu-id="62fa5-113">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="62fa5-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62fa5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="62fa5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62fa5-115">**акцессиблечилдрен**</span><span class="sxs-lookup"><span data-stu-id="62fa5-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 





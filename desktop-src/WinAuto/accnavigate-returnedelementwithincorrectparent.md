---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: Аккнавигате \_ ретурнеделементвисинкорректпарент
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104558773"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="ae31e-103">Аккнавигате \_ ретурнеделементвисинкорректпарент</span><span class="sxs-lookup"><span data-stu-id="ae31e-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="ae31e-104">Текст</span><span class="sxs-lookup"><span data-stu-id="ae31e-104">Text</span></span>

<span data-ttu-id="ae31e-105">Вызов Аккнавигате ((Live Search), 0, НАВДИР \_ FIRSTCHILD) вернул (x-Gadget:///gadget.html) неверный родительский элемент ( \[ null \] ), а не (динамический поиск)</span><span class="sxs-lookup"><span data-stu-id="ae31e-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="ae31e-106">Тип</span><span class="sxs-lookup"><span data-stu-id="ae31e-106">Type</span></span>

<span data-ttu-id="ae31e-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="ae31e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ae31e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ae31e-108">Description</span></span>

<span data-ttu-id="ae31e-109">При вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочернего элемента, возвращенного [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (с помощью \_ констант навигации навдир FIRSTCHILD или навдир \_ LASTCHILD), возвращаемый родительский элемент не соответствует родительскому элементу, указанному в вызове **аккнавигате** .</span><span class="sxs-lookup"><span data-stu-id="ae31e-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![Пример недопустимой реализации MSAA, возвращающей неверный родительский элемент.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="ae31e-111">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="ae31e-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ae31e-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="ae31e-112">Possible causes</span></span>

<span data-ttu-id="ae31e-113">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="ae31e-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae31e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ae31e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae31e-115">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="ae31e-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="ae31e-116">**IAccessible:: Get \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="ae31e-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 





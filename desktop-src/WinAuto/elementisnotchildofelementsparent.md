---
title: елементиснотчилдофелементспарент
description: елементиснотчилдофелементспарент
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411436"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="d06ca-103">елементиснотчилдофелементспарент</span><span class="sxs-lookup"><span data-stu-id="d06ca-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="d06ca-104">Текст</span><span class="sxs-lookup"><span data-stu-id="d06ca-104">Text</span></span>

<span data-ttu-id="d06ca-105">Элемент не является дочерним элементом родительского элемента</span><span class="sxs-lookup"><span data-stu-id="d06ca-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="d06ca-106">Тип</span><span class="sxs-lookup"><span data-stu-id="d06ca-106">Type</span></span>

<span data-ttu-id="d06ca-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="d06ca-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="d06ca-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d06ca-108">Description</span></span>

<span data-ttu-id="d06ca-109">При вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочернего элемента, возвращенного [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (с помощью \_ констант навигации навдир FIRSTCHILD или навдир \_ LASTCHILD), возвращаемый родительский элемент не соответствует родительскому элементу, указанному в вызове **аккнавигате** .</span><span class="sxs-lookup"><span data-stu-id="d06ca-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="d06ca-110">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="d06ca-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d06ca-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="d06ca-111">Possible causes</span></span>

<span data-ttu-id="d06ca-112">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="d06ca-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d06ca-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d06ca-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d06ca-114">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="d06ca-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="d06ca-115">**IAccessible:: Get \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="d06ca-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 





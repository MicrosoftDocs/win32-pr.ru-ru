---
title: нуллпарент
description: нуллпарент
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329656"
---
# <a name="nullparent"></a><span data-ttu-id="8dcd7-103">нуллпарент</span><span class="sxs-lookup"><span data-stu-id="8dcd7-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="8dcd7-104">Текст</span><span class="sxs-lookup"><span data-stu-id="8dcd7-104">Text</span></span>

<span data-ttu-id="8dcd7-105">Родительский элемент Elements имеет значение NULL</span><span class="sxs-lookup"><span data-stu-id="8dcd7-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="8dcd7-106">Тип</span><span class="sxs-lookup"><span data-stu-id="8dcd7-106">Type</span></span>

<span data-ttu-id="8dcd7-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="8dcd7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8dcd7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8dcd7-108">Description</span></span>

<span data-ttu-id="8dcd7-109">Значение NULL возвращается при вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для элемента.</span><span class="sxs-lookup"><span data-stu-id="8dcd7-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="8dcd7-110">Метод **Get \_ аккпарент** должен возвращать значение NULL только при вызове в корневом элементе целевого объекта проверки.</span><span class="sxs-lookup"><span data-stu-id="8dcd7-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="8dcd7-111">Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="8dcd7-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8dcd7-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="8dcd7-112">Possible causes</span></span>

<span data-ttu-id="8dcd7-113">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="8dcd7-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dcd7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8dcd7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcd7-115">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="8dcd7-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="8dcd7-116">**IAccessible:: Get \_ аккпарент**</span><span class="sxs-lookup"><span data-stu-id="8dcd7-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 





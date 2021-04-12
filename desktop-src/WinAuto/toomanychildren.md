---
title: туманичилдрен
description: туманичилдрен
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253347"
---
# <a name="toomanychildren"></a><span data-ttu-id="ff331-103">туманичилдрен</span><span class="sxs-lookup"><span data-stu-id="ff331-103">TooManyChildren</span></span>

## <a name="text"></a><span data-ttu-id="ff331-104">Текст</span><span class="sxs-lookup"><span data-stu-id="ff331-104">Text</span></span>

<span data-ttu-id="ff331-105">Остановлен Поиск дополнительных элементов того же уровня после поиска {0} элементов того же уровня.</span><span class="sxs-lookup"><span data-stu-id="ff331-105">Stopped looking for additional siblings after finding {0} siblings.</span></span> <span data-ttu-id="ff331-106">Возможно, неверное дерево</span><span class="sxs-lookup"><span data-stu-id="ff331-106">Possible incorrect tree</span></span>

## <a name="type"></a><span data-ttu-id="ff331-107">Тип</span><span class="sxs-lookup"><span data-stu-id="ff331-107">Type</span></span>

<span data-ttu-id="ff331-108">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="ff331-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="ff331-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ff331-109">Description</span></span>

<span data-ttu-id="ff331-110">Дерево элементов может быть циклическим и неограниченным глубиной дерева.</span><span class="sxs-lookup"><span data-stu-id="ff331-110">The element tree might be cyclic and the tree depth infinite.</span></span>

<span data-ttu-id="ff331-111">Эта проблема может вызвать проблемы с навигацией для автоматизированных инструментов, так как они вводят циклическую ссылку или бесконечный цикл.</span><span class="sxs-lookup"><span data-stu-id="ff331-111">This issue can cause navigation problems for automated tools because they will enter what appears to be a circular reference or infinite loop.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ff331-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="ff331-112">Possible causes</span></span>

-   <span data-ttu-id="ff331-113">Проект приложения или элемента управления может быть слишком сложным.</span><span class="sxs-lookup"><span data-stu-id="ff331-113">Application or control design may be too complex.</span></span> <span data-ttu-id="ff331-114">Это предупреждение может быть получено для элементов управления "представление списка", имеющих большое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="ff331-114">This warning might be reported for list-view controls that have a large number of items.</span></span> <span data-ttu-id="ff331-115">В таких случаях это предупреждение обычно можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="ff331-115">In these cases, you can typically ignore this warning.</span></span>
-   <span data-ttu-id="ff331-116">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="ff331-116">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff331-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ff331-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff331-118">**IAccessible:: Аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="ff331-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 





---
description: Приложение объединяет два региона, вызывая функцию Комбинергн.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Объединение регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553964"
---
# <a name="combining-regions"></a><span data-ttu-id="f922d-103">Объединение регионов</span><span class="sxs-lookup"><span data-stu-id="f922d-103">Combining Regions</span></span>

<span data-ttu-id="f922d-104">Приложение объединяет два региона, вызывая функцию [**комбинергн**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .</span><span class="sxs-lookup"><span data-stu-id="f922d-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="f922d-105">С помощью этой функции приложение может сочетать пересекающиеся части двух регионов, все, кроме пересекающихся частей двух регионов, две исходные области целиком и т. д.</span><span class="sxs-lookup"><span data-stu-id="f922d-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="f922d-106">Ниже приведены пять значений, определяющих сочетания областей.</span><span class="sxs-lookup"><span data-stu-id="f922d-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="f922d-107">Значение</span><span class="sxs-lookup"><span data-stu-id="f922d-107">Value</span></span>     | <span data-ttu-id="f922d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f922d-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f922d-109">РГН \_ и</span><span class="sxs-lookup"><span data-stu-id="f922d-109">RGN\_AND</span></span>  | <span data-ttu-id="f922d-110">Пересекающиеся части двух исходных регионов определяют новый регион.</span><span class="sxs-lookup"><span data-stu-id="f922d-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="f922d-111">\_копирование РГН</span><span class="sxs-lookup"><span data-stu-id="f922d-111">RGN\_COPY</span></span> | <span data-ttu-id="f922d-112">Копия первого (из двух исходных регионов) определяет новый регион.</span><span class="sxs-lookup"><span data-stu-id="f922d-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="f922d-113">РГН \_ diff</span><span class="sxs-lookup"><span data-stu-id="f922d-113">RGN\_DIFF</span></span> | <span data-ttu-id="f922d-114">Часть первого региона, который не пересекается со вторым, определяет новый регион.</span><span class="sxs-lookup"><span data-stu-id="f922d-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="f922d-115">РГН \_ или</span><span class="sxs-lookup"><span data-stu-id="f922d-115">RGN\_OR</span></span>   | <span data-ttu-id="f922d-116">Два исходных региона определяют новый регион.</span><span class="sxs-lookup"><span data-stu-id="f922d-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="f922d-117">РГН \_ XOR</span><span class="sxs-lookup"><span data-stu-id="f922d-117">RGN\_XOR</span></span>  | <span data-ttu-id="f922d-118">Эти части двух исходных регионов, которые не перекрываются, определяют новый регион.</span><span class="sxs-lookup"><span data-stu-id="f922d-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="f922d-119">На следующем рисунке показаны пять возможных сочетаний квадрата и круговой области, полученной в результате вызова [**комбинергн**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span><span class="sxs-lookup"><span data-stu-id="f922d-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![Иллюстрация, демонстрирующая результаты, описанные в предыдущей таблице](images/csrgn-02.png)

 

 




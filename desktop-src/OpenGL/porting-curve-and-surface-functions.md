---
title: Перенос функций кривой и поверхностей
description: Перенос функций кривой и поверхностей
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Перенос GL по IRI, кривые
- Перенос из IRI GL, кривых
- перенос в OpenGL из IRI GL, кривых
- Перенос по стандарту OpenGL из IRI GL, кривых
- Перенос GL по IRI, исправления поверхности
- Перенос из IRI GL, исправления поверхности
- перенос в OpenGL из IRI GL, исправления поверхности
- Перенос по стандарту OpenGL из IRI GL, исправления поверхности
- кривые
- исправления в Surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328827"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="421b4-113">Перенос функций кривой и поверхностей</span><span class="sxs-lookup"><span data-stu-id="421b4-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="421b4-114">OpenGL не поддерживает эквиваленты функций IRI GL для кривых и исправлений на поверхности.</span><span class="sxs-lookup"><span data-stu-id="421b4-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="421b4-115">Вам потребуется переписать код, если он включает любой из следующих вызовов:</span><span class="sxs-lookup"><span data-stu-id="421b4-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="421b4-116">**дефбасис**</span><span class="sxs-lookup"><span data-stu-id="421b4-116">**defbasis**</span></span>
-   <span data-ttu-id="421b4-117">**курвебасис**, **курвепреЦисион**, **КРВ**, **крвн**, **ркрв**, **ркрвн** и **курвеит**</span><span class="sxs-lookup"><span data-stu-id="421b4-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="421b4-118">**патчбасис**, **патчкурвес**, **патчпреЦисион**, **Patch** и **рпатч**</span><span class="sxs-lookup"><span data-stu-id="421b4-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="421b4-119">Этот раздел содержит сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="421b4-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="421b4-120">Перенос объектов НУРБС</span><span class="sxs-lookup"><span data-stu-id="421b4-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="421b4-121">Перенос кривых НУРБС</span><span class="sxs-lookup"><span data-stu-id="421b4-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="421b4-122">Перенос кривых обрезки</span><span class="sxs-lookup"><span data-stu-id="421b4-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="421b4-123">Перенос поверхностей НУРБС</span><span class="sxs-lookup"><span data-stu-id="421b4-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 





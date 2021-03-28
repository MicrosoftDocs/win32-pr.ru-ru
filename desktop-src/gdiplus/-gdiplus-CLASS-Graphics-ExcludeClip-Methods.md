---
description: В этом разделе перечислены методы Ексклудеклип класса Graphics. Полный список методов для класса Graphics см. в разделе Graphics.
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: Методы Graphics. Ексклудеклип (Гдиплусграфикс. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998891"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="020b4-104">Методы Graphics. Ексклудеклип</span><span class="sxs-lookup"><span data-stu-id="020b4-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="020b4-105">В этом разделе перечислены методы Ексклудеклип класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="020b4-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="020b4-106">Полный список методов для класса **Graphics** см. в разделе [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="020b4-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="020b4-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="020b4-107">Overload list</span></span>



| <span data-ttu-id="020b4-108">Метод</span><span class="sxs-lookup"><span data-stu-id="020b4-108">Method</span></span>                                                                         | <span data-ttu-id="020b4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="020b4-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020b4-110">[**Ексклудеклип (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="020b4-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="020b4-111">Метод [**Graphics:: ексклудеклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) обновляет область отсечения до части, которая не пересекается с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="020b4-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="020b4-112">[**Ексклудеклип (Ректф&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="020b4-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="020b4-113">Метод [**Graphics:: ексклудеклип**](/previous-versions//ms535975(v=vs.85)) обновляет область отсечения до части, которая не пересекается с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="020b4-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="020b4-114">[**Ексклудеклип (регион \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="020b4-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="020b4-115">Метод [**Graphics:: ексклудеклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) обновляет область отсечения с той частью, которая не перекрывает указанную область.</span><span class="sxs-lookup"><span data-stu-id="020b4-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="020b4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="020b4-116">Requirements</span></span>



| <span data-ttu-id="020b4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="020b4-117">Requirement</span></span> | <span data-ttu-id="020b4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="020b4-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="020b4-119">Header</span><span class="sxs-lookup"><span data-stu-id="020b4-119">Header</span></span><br/> | <dl> <span data-ttu-id="020b4-120"><dt>Гдиплусграфикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="020b4-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 

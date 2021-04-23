---
description: Предоставляет методы и свойства для региона, представляющего область документа.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Интерфейс Ианалисисрегион (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810043"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="80406-103">Интерфейс Ианалисисрегион</span><span class="sxs-lookup"><span data-stu-id="80406-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="80406-104">Предоставляет методы и свойства для региона, представляющего область документа.</span><span class="sxs-lookup"><span data-stu-id="80406-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="80406-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="80406-105">Members</span></span>

<span data-ttu-id="80406-106">Интерфейс **ианалисисрегион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80406-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80406-107">**Ианалисисрегион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="80406-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="80406-108">Методы</span><span class="sxs-lookup"><span data-stu-id="80406-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80406-109">Методы</span><span class="sxs-lookup"><span data-stu-id="80406-109">Methods</span></span>

<span data-ttu-id="80406-110">Интерфейс **ианалисисрегион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="80406-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="80406-111">Метод</span><span class="sxs-lookup"><span data-stu-id="80406-111">Method</span></span>                                                           | <span data-ttu-id="80406-112">Описание</span><span class="sxs-lookup"><span data-stu-id="80406-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80406-113">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="80406-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="80406-114">Создает копию **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="80406-115">**ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="80406-116">Ограничивающий область **ианалисисрегион** до части области, которая не пересекается с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="80406-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="80406-117">**ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="80406-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="80406-118">Ограничивающий область **ианалисисрегион** до части области, которая не пересекается с заданным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="80406-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="80406-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="80406-120">Извлекает ограничивающий прямоугольник **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="80406-121">**жетрегионсканс**</span><span class="sxs-lookup"><span data-stu-id="80406-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="80406-122">Извлекает массив прямоугольников, определяющих площадь **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="80406-123">**интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="80406-124">Область этого **ианалисисрегиона** ограничена областью, созданной ее пересечением с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="80406-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="80406-125">**интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="80406-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="80406-126">Область **ианалисисрегион** ограничена областью, созданной ее пересечением, с указанным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="80406-127">**интерсектсвис**</span><span class="sxs-lookup"><span data-stu-id="80406-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="80406-128">Определяет, пересекаются ли области **ианалисисрегион** с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="80406-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="80406-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="80406-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="80406-130">Получает значение, указывающее, представляет ли **ианалисисрегион** пустой регион.</span><span class="sxs-lookup"><span data-stu-id="80406-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="80406-131">**Бесконечность**</span><span class="sxs-lookup"><span data-stu-id="80406-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="80406-132">Извлекает значение, указывающее, представляет ли **ианалисисрегион** неограниченную область.</span><span class="sxs-lookup"><span data-stu-id="80406-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="80406-133">**макимпти**</span><span class="sxs-lookup"><span data-stu-id="80406-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="80406-134">Сокращает **ианалисисрегион** для представления пустой области.</span><span class="sxs-lookup"><span data-stu-id="80406-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="80406-135">**макеинфините**</span><span class="sxs-lookup"><span data-stu-id="80406-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="80406-136">Разворачивает **ианалисисрегион** для представления бесконечной области.</span><span class="sxs-lookup"><span data-stu-id="80406-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="80406-137">**унионректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="80406-138">Разворачивает область этого **ианалисисрегиона** в область, созданную его объединением с указанным прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="80406-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="80406-139">**унионрегион**</span><span class="sxs-lookup"><span data-stu-id="80406-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="80406-140">Разворачивает область этого **ианалисисрегиона** в область, созданную с помощью объединения, с указанным **ианалисисрегион**.</span><span class="sxs-lookup"><span data-stu-id="80406-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="80406-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80406-141">Remarks</span></span>

<span data-ttu-id="80406-142">Этот интерфейс представляет область, созданную из прямоугольных областей.</span><span class="sxs-lookup"><span data-stu-id="80406-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="80406-143">[**Иинканализер**](iinkanalyzer.md) Возвращает или интерпретирует координаты области в пространстве координат, в котором она получает данные росчерка.</span><span class="sxs-lookup"><span data-stu-id="80406-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="80406-144">Чтобы получить текущие границы **ианалисисрегион**, используйте метод [**ианалисисрегион::**](ianalysisregion-getbounds.md) или [**метод ианалисисрегион:: жетрегионсканс**](ianalysisregion-getregionscans.md).</span><span class="sxs-lookup"><span data-stu-id="80406-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="80406-145">Чтобы изменить область существующего **ианалисисрегион**, используйте следующие методы.</span><span class="sxs-lookup"><span data-stu-id="80406-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="80406-146">**Ианалисисрегион:: Ексклудеректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="80406-147">**Метод Ианалисисрегион:: Ексклудерегион**</span><span class="sxs-lookup"><span data-stu-id="80406-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="80406-148">**Метод Ианалисисрегион:: Интерсектректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="80406-149">**Метод Ианалисисрегион:: Интерсектрегион**</span><span class="sxs-lookup"><span data-stu-id="80406-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="80406-150">**Метод Ианалисисрегион:: Макимпти**</span><span class="sxs-lookup"><span data-stu-id="80406-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="80406-151">**Метод Ианалисисрегион:: Макеинфините**</span><span class="sxs-lookup"><span data-stu-id="80406-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="80406-152">**Метод Ианалисисрегион:: Унионректангле**</span><span class="sxs-lookup"><span data-stu-id="80406-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="80406-153">**Метод Ианалисисрегион:: Унионрегион**</span><span class="sxs-lookup"><span data-stu-id="80406-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="80406-154">Этот интерфейс эквивалентен классу System. Windows. Ink. Аналисискоре. Аналисисрегионбасе в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="80406-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="80406-155">Требования</span><span class="sxs-lookup"><span data-stu-id="80406-155">Requirements</span></span>



| <span data-ttu-id="80406-156">Требование</span><span class="sxs-lookup"><span data-stu-id="80406-156">Requirement</span></span> | <span data-ttu-id="80406-157">Значение</span><span class="sxs-lookup"><span data-stu-id="80406-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80406-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80406-158">Minimum supported client</span></span><br/> | <span data-ttu-id="80406-159">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="80406-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="80406-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80406-160">Minimum supported server</span></span><br/> | <span data-ttu-id="80406-161">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80406-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="80406-162">Header</span><span class="sxs-lookup"><span data-stu-id="80406-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="80406-163"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="80406-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="80406-164">DLL</span><span class="sxs-lookup"><span data-stu-id="80406-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80406-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80406-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="80406-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80406-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80406-167">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="80406-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="80406-168">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="80406-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 


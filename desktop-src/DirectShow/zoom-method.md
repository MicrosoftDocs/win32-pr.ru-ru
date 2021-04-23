---
description: Метод Zoom позволяет увеличить или уменьшить отображаемое изображение, Центрированное по заданному набору экранных координат.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Метод Zoom
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497982"
---
# <a name="zoom-method"></a><span data-ttu-id="56f0d-103">Метод Zoom</span><span class="sxs-lookup"><span data-stu-id="56f0d-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="56f0d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56f0d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="56f0d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="56f0d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="56f0d-106">`Zoom`Метод позволяет увеличить или уменьшить отображаемое изображение, Центрированное по заданному набору экранных координат.</span><span class="sxs-lookup"><span data-stu-id="56f0d-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="56f0d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="56f0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f0d-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*икспос*</span><span class="sxs-lookup"><span data-stu-id="56f0d-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="56f0d-109">Задает координату x в центре прямоугольной области масштабирования в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="56f0d-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="56f0d-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*ийпос*</span><span class="sxs-lookup"><span data-stu-id="56f0d-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="56f0d-111">Задает координату по оси y в центре прямоугольника для масштабирования в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="56f0d-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="56f0d-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*изумратио*</span><span class="sxs-lookup"><span data-stu-id="56f0d-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="56f0d-113">Задает коэффициент увеличения, применяемый к текущему значению масштаба в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="56f0d-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="56f0d-114">Общее максимальное значение зависит от того, что может поддерживать наложение оборудования; Обычно это фактор в 32 – 64 раза больше исходного размера.</span><span class="sxs-lookup"><span data-stu-id="56f0d-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f0d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56f0d-115">Return Value</span></span>

<span data-ttu-id="56f0d-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="56f0d-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f0d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56f0d-117">Remarks</span></span>

<span data-ttu-id="56f0d-118">Новое соотношение масштаба действует до тех пор, пока оно не будет восстановлено до исходного размера или опять не изменится.</span><span class="sxs-lookup"><span data-stu-id="56f0d-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="56f0d-119">Иными словами, два вызова этого метода, указывающие на *изумратио* двух, будут соотношение масштаба в четыре раза больше, чем исходный размер видео.</span><span class="sxs-lookup"><span data-stu-id="56f0d-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="56f0d-120">Если пользователь пытается увеличить масштаб, который может поддерживаться оборудованием, этот метод завершится удачно, но ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="56f0d-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="56f0d-121">Метод [**сетклипвидеорект**](setclipvideorect-method.md) — еще один способ увеличить масштаб. Единственное различие между двумя методами заключается в способе указания прямоугольника масштаба.</span><span class="sxs-lookup"><span data-stu-id="56f0d-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 




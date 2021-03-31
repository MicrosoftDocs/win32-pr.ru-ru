---
description: Метод Сетклипвидеорект позволяет увеличить изображение экрана до указанного подпрямоугольника.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Метод Сетклипвидеорект
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805872"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="5f6b9-103">Метод Сетклипвидеорект</span><span class="sxs-lookup"><span data-stu-id="5f6b9-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="5f6b9-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5f6b9-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5f6b9-106">`SetClipVideoRect`Метод позволяет увеличить изображение экрана до указанного подпрямоугольника.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="5f6b9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f6b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f6b9-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*орект*</span><span class="sxs-lookup"><span data-stu-id="5f6b9-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="5f6b9-109">Задает объект [двдрект](dvdrect-object.md) , который содержит прямоугольник обрезки.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f6b9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f6b9-110">Return Value</span></span>

<span data-ttu-id="5f6b9-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f6b9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f6b9-112">Remarks</span></span>

<span data-ttu-id="5f6b9-113">При установке нового прямоугольника обрезки объект увеличивает эту область в соответствии с общими отображаемыми размерами приложения.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="5f6b9-114">Это приведет к уменьшению масштаба в определенной области экрана.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="5f6b9-115">Чтобы указать прямоугольник, создайте новый объект [двдрект](dvdrect-object.md) и заполните его свойства.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="5f6b9-116">Наиболее распространенный прямоугольник для экрана видео — 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="5f6b9-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f6b9-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f6b9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6b9-118">**жетклипвидеорект**</span><span class="sxs-lookup"><span data-stu-id="5f6b9-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 




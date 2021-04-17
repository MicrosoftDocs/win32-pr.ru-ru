---
description: Метод Жетпалеттеверсион извлекает текущую версию палитры.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Кдравимаже. Жетпалеттеверсион, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679864"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="210e8-103">Кдравимаже. Жетпалеттеверсион, метод</span><span class="sxs-lookup"><span data-stu-id="210e8-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="210e8-104">`GetPaletteVersion`Метод получает текущую версию палитры.</span><span class="sxs-lookup"><span data-stu-id="210e8-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="210e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="210e8-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="210e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="210e8-106">Parameters</span></span>

<span data-ttu-id="210e8-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="210e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="210e8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="210e8-108">Return value</span></span>

<span data-ttu-id="210e8-109">Возвращает значение переменной члена **m \_ палеттеверсион** .</span><span class="sxs-lookup"><span data-stu-id="210e8-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="210e8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="210e8-110">Remarks</span></span>

<span data-ttu-id="210e8-111">Значение, возвращаемое этим методом, применяется только в том случае, если распределитель является объектом [**Цимажеаллокатор**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="210e8-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="210e8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="210e8-112">Requirements</span></span>



| <span data-ttu-id="210e8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="210e8-113">Requirement</span></span> | <span data-ttu-id="210e8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="210e8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210e8-115">Header</span><span class="sxs-lookup"><span data-stu-id="210e8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="210e8-116"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="210e8-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="210e8-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="210e8-117">Library</span></span><br/> | <dl> <span data-ttu-id="210e8-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="210e8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="210e8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="210e8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210e8-120">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="210e8-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="210e8-121">**Кдравимаже:: Инкрементпалеттеверсион**</span><span class="sxs-lookup"><span data-stu-id="210e8-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="210e8-122">**Кдравимаже:: Ресетпалеттеверсион**</span><span class="sxs-lookup"><span data-stu-id="210e8-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 





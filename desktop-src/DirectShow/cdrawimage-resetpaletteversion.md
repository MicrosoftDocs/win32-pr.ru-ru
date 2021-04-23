---
description: Метод Ресетпалеттеверсион сбрасывает версию палитры. Вызывайте этот метод, если ПИН-код фильтра владельца повторно подключится.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Кдравимаже. Ресетпалеттеверсион, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657145"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="85fbb-104">Кдравимаже. Ресетпалеттеверсион, метод</span><span class="sxs-lookup"><span data-stu-id="85fbb-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="85fbb-105">`ResetPaletteVersion`Метод сбрасывает версию палитры.</span><span class="sxs-lookup"><span data-stu-id="85fbb-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="85fbb-106">Вызывайте этот метод, если ПИН-код фильтра владельца повторно подключится.</span><span class="sxs-lookup"><span data-stu-id="85fbb-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="85fbb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85fbb-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="85fbb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85fbb-108">Parameters</span></span>

<span data-ttu-id="85fbb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="85fbb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85fbb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85fbb-110">Return value</span></span>

<span data-ttu-id="85fbb-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85fbb-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85fbb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85fbb-112">Remarks</span></span>

<span data-ttu-id="85fbb-113">Этот метод устанавливает значение **m \_ палеттеверсион** в стандартную константу, **\_ версию палитры**.</span><span class="sxs-lookup"><span data-stu-id="85fbb-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85fbb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="85fbb-114">Requirements</span></span>



| <span data-ttu-id="85fbb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="85fbb-115">Requirement</span></span> | <span data-ttu-id="85fbb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="85fbb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fbb-117">Header</span><span class="sxs-lookup"><span data-stu-id="85fbb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="85fbb-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85fbb-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85fbb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85fbb-119">Library</span></span><br/> | <dl> <span data-ttu-id="85fbb-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="85fbb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85fbb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85fbb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85fbb-122">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="85fbb-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="85fbb-123">**Кдравимаже:: Жетпалеттеверсион**</span><span class="sxs-lookup"><span data-stu-id="85fbb-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="85fbb-124">**Кдравимаже:: Инкрементпалеттеверсион**</span><span class="sxs-lookup"><span data-stu-id="85fbb-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 





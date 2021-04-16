---
description: Метод Скалесаурцерект масштабирует прямоугольник, если существует разница между собственным размером видео и форматом типа мультимедиа.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Кдравимаже. Скалесаурцерект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665272"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="b4a07-103">Кдравимаже. Скалесаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="b4a07-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="b4a07-104">`ScaleSourceRect`Метод масштабирует прямоугольник, если существует разница между собственным размером видео и форматом типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b4a07-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4a07-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="b4a07-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a07-107">*псаурце*</span><span class="sxs-lookup"><span data-stu-id="b4a07-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a07-108">Указатель на немасштабируемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="b4a07-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a07-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4a07-109">Return value</span></span>

<span data-ttu-id="b4a07-110">Возвращает масштабируемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="b4a07-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a07-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4a07-111">Remarks</span></span>

<span data-ttu-id="b4a07-112">В классе **кдравимаже** этот метод возвращает *псаурце* без каких бы то ни было изменений.</span><span class="sxs-lookup"><span data-stu-id="b4a07-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="b4a07-113">Этот метод можно переопределить, если фильтр растягивает входящее изображение видео.</span><span class="sxs-lookup"><span data-stu-id="b4a07-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="b4a07-114">Например, размер собственного видео может быть 320 240, но тип носителя для входного ПИН-кода может быть 640 480.</span><span class="sxs-lookup"><span data-stu-id="b4a07-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="b4a07-115">В этом случае фильтру потребуется масштабировать исходный прямоугольник с коэффициентом 2.</span><span class="sxs-lookup"><span data-stu-id="b4a07-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a07-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b4a07-116">Requirements</span></span>



| <span data-ttu-id="b4a07-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b4a07-117">Requirement</span></span> | <span data-ttu-id="b4a07-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b4a07-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a07-119">Header</span><span class="sxs-lookup"><span data-stu-id="b4a07-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b4a07-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a07-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4a07-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4a07-121">Library</span></span><br/> | <dl> <span data-ttu-id="b4a07-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a07-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a07-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4a07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a07-124">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="b4a07-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





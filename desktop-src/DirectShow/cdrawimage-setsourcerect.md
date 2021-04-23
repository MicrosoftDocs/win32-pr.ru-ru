---
description: Метод Сетсаурцерект задает исходный прямоугольник.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Кдравимаже. Сетсаурцерект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665248"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="f6aed-103">Кдравимаже. Сетсаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="f6aed-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="f6aed-104">`SetSourceRect`Метод задает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f6aed-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6aed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6aed-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="f6aed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6aed-107">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="f6aed-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f6aed-108">Указатель на структуру **Rect** , определяющую новый исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f6aed-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6aed-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6aed-109">Return value</span></span>

<span data-ttu-id="f6aed-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f6aed-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6aed-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6aed-111">Remarks</span></span>

<span data-ttu-id="f6aed-112">Фильтр-владелец должен вызывать этот метод, если исходный прямоугольник изменяется; Например, в ответ на вызов [**ибасиквидео:: сетсаурцепоситион**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .</span><span class="sxs-lookup"><span data-stu-id="f6aed-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="f6aed-113">Проверьте прямоугольник, указанный в *псаурцерект* , перед вызовом этого метода, чтобы убедиться, что он не выходит за пределы собственного видео.</span><span class="sxs-lookup"><span data-stu-id="f6aed-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6aed-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6aed-114">Requirements</span></span>



| <span data-ttu-id="f6aed-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6aed-115">Requirement</span></span> | <span data-ttu-id="f6aed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6aed-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6aed-117">Header</span><span class="sxs-lookup"><span data-stu-id="f6aed-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f6aed-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6aed-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6aed-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6aed-119">Library</span></span><br/> | <dl> <span data-ttu-id="f6aed-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f6aed-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6aed-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6aed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6aed-122">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="f6aed-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





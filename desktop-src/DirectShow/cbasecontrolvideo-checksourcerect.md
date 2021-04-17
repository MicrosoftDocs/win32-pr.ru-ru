---
description: Определяет, является ли исходный прямоугольник допустимым.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Кбасеконтролвидео. Чекксаурцерект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657251"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="0ef54-103">Кбасеконтролвидео. Чекксаурцерект, метод</span><span class="sxs-lookup"><span data-stu-id="0ef54-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="0ef54-104">Определяет, является ли исходный прямоугольник допустимым.</span><span class="sxs-lookup"><span data-stu-id="0ef54-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ef54-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="0ef54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ef54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef54-107">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="0ef54-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="0ef54-108">Указатель на исходный прямоугольник для проверки.</span><span class="sxs-lookup"><span data-stu-id="0ef54-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef54-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ef54-109">Return value</span></span>

<span data-ttu-id="0ef54-110">Возвращает значение E \_ INVALIDARG, если недопустимо; в противном случае возвращает значение \_ "Error" (ОК).</span><span class="sxs-lookup"><span data-stu-id="0ef54-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef54-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ef54-111">Remarks</span></span>

<span data-ttu-id="0ef54-112">Эта функция члена проверяет, что запрошенный исходный прямоугольник не превышает доступный исходный видеоролик.</span><span class="sxs-lookup"><span data-stu-id="0ef54-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="0ef54-113">Координаты Left и Top не могут быть отрицательными, а ширина и высота не могут превышать правую и нижнюю часть видео.</span><span class="sxs-lookup"><span data-stu-id="0ef54-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef54-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0ef54-114">Requirements</span></span>



| <span data-ttu-id="0ef54-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0ef54-115">Requirement</span></span> | <span data-ttu-id="0ef54-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0ef54-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef54-117">Header</span><span class="sxs-lookup"><span data-stu-id="0ef54-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef54-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef54-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ef54-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ef54-119">Library</span></span><br/> | <dl> <span data-ttu-id="0ef54-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef54-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef54-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ef54-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef54-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="0ef54-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: Метод Чекктаржетрект определяет, является ли целевой прямоугольник допустимым.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Кбасеконтролвидео. Чекктаржетрект, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688773"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="ef1bf-103">Кбасеконтролвидео. Чекктаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="ef1bf-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="ef1bf-104">`CheckTargetRect`Метод определяет, является ли целевой прямоугольник допустимым.</span><span class="sxs-lookup"><span data-stu-id="ef1bf-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef1bf-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="ef1bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef1bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1bf-107">*птаржетрект*</span><span class="sxs-lookup"><span data-stu-id="ef1bf-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="ef1bf-108">Указатель на целевой прямоугольник для проверки.</span><span class="sxs-lookup"><span data-stu-id="ef1bf-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1bf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef1bf-109">Return value</span></span>

<span data-ttu-id="ef1bf-110">Возвращает значение E \_ INVALIDARG, если недопустимо; в противном случае возвращает значение \_ "Error" (ОК).</span><span class="sxs-lookup"><span data-stu-id="ef1bf-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1bf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef1bf-111">Remarks</span></span>

<span data-ttu-id="ef1bf-112">Эта функция-член определяет, является ли запрошенный целевой прямоугольник допустимым.</span><span class="sxs-lookup"><span data-stu-id="ef1bf-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="ef1bf-113">Так как конечный прямоугольник указывает на расположение в логическом клиенте окна, координаты могут быть отрицательными, хотя общая ширина и высота не могут быть равны нулю или отрицательному значению.</span><span class="sxs-lookup"><span data-stu-id="ef1bf-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1bf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ef1bf-114">Requirements</span></span>



| <span data-ttu-id="ef1bf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ef1bf-115">Requirement</span></span> | <span data-ttu-id="ef1bf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1bf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1bf-117">Header</span><span class="sxs-lookup"><span data-stu-id="ef1bf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ef1bf-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef1bf-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef1bf-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef1bf-119">Library</span></span><br/> | <dl> <span data-ttu-id="ef1bf-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ef1bf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1bf-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef1bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1bf-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="ef1bf-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





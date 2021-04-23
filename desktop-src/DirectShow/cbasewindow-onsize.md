---
description: Метод OnSize обрабатывает \_ сообщения размером WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Метод Кбасевиндов. OnSize (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675087"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="d0ea3-103">Кбасевиндов. OnSize, метод</span><span class="sxs-lookup"><span data-stu-id="d0ea3-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="d0ea3-104">`OnSize`Метод обрабатывает \_ сообщения размером WM.</span><span class="sxs-lookup"><span data-stu-id="d0ea3-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ea3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0ea3-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="d0ea3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0ea3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ea3-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="d0ea3-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ea3-108">Ширина клиентской области в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d0ea3-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d0ea3-109">*Height*</span><span class="sxs-lookup"><span data-stu-id="d0ea3-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="d0ea3-110">Высота клиентской области в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d0ea3-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ea3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0ea3-111">Return value</span></span>

<span data-ttu-id="d0ea3-112">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d0ea3-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ea3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0ea3-113">Remarks</span></span>

<span data-ttu-id="d0ea3-114">Этот метод сохраняет новую ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="d0ea3-114">This method stores the new width and height.</span></span> <span data-ttu-id="d0ea3-115">Чтобы получить эти значения, вызовите методы [**кбасевиндов:: жетвиндовхеигхт**](cbasewindow-getwindowheight.md) и [**Кбасевиндов:: жетвиндоввидс**](cbasewindow-getwindowwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="d0ea3-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ea3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d0ea3-116">Requirements</span></span>



| <span data-ttu-id="d0ea3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d0ea3-117">Requirement</span></span> | <span data-ttu-id="d0ea3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d0ea3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ea3-119">Header</span><span class="sxs-lookup"><span data-stu-id="d0ea3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d0ea3-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0ea3-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0ea3-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0ea3-121">Library</span></span><br/> | <dl> <span data-ttu-id="d0ea3-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d0ea3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ea3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0ea3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ea3-124">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="d0ea3-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 





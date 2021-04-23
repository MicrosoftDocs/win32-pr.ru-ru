---
description: Метод OnClose обрабатывает сообщения WM \_ Close.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Метод Кбасевиндов. OnClose (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657039"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="59af7-103">Метод Кбасевиндов. OnClose</span><span class="sxs-lookup"><span data-stu-id="59af7-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="59af7-104">`OnClose`Метод обрабатывает сообщения WM \_ Close.</span><span class="sxs-lookup"><span data-stu-id="59af7-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="59af7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59af7-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="59af7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59af7-106">Parameters</span></span>

<span data-ttu-id="59af7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="59af7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59af7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59af7-108">Return value</span></span>

<span data-ttu-id="59af7-109">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="59af7-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59af7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59af7-110">Remarks</span></span>

<span data-ttu-id="59af7-111">В базовом классе этот метод просто скрывает окно.</span><span class="sxs-lookup"><span data-stu-id="59af7-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="59af7-112">Как правило, производный класс переопределяет этот метод, чтобы он также отправлял событие [**EC \_ усераборт**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="59af7-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="59af7-113">Не переопределяйте метод, чтобы уничтожить окно.</span><span class="sxs-lookup"><span data-stu-id="59af7-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="59af7-114">Вместо этого вызовите метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) при уничтожении фильтра-владельца.</span><span class="sxs-lookup"><span data-stu-id="59af7-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59af7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="59af7-115">Requirements</span></span>



| <span data-ttu-id="59af7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="59af7-116">Requirement</span></span> | <span data-ttu-id="59af7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="59af7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59af7-118">Header</span><span class="sxs-lookup"><span data-stu-id="59af7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="59af7-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59af7-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59af7-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59af7-120">Library</span></span><br/> | <dl> <span data-ttu-id="59af7-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="59af7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59af7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59af7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59af7-123">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="59af7-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 





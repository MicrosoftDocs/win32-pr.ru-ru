---
description: Метод Перформанцеалигнвиндов совмещает расположение окна до границ DWORD, что обеспечивает максимальную производительность.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Кбасевиндов. Перформанцеалигнвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679852"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="9d723-103">Кбасевиндов. Перформанцеалигнвиндов, метод</span><span class="sxs-lookup"><span data-stu-id="9d723-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="9d723-104">`PerformanceAlignWindow`Метод совмещает расположение окна до границ **DWORD** , что обеспечивает максимальную производительность.</span><span class="sxs-lookup"><span data-stu-id="9d723-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d723-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d723-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="9d723-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d723-106">Parameters</span></span>

<span data-ttu-id="9d723-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9d723-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d723-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d723-108">Return value</span></span>

<span data-ttu-id="9d723-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9d723-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d723-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d723-110">Remarks</span></span>

<span data-ttu-id="9d723-111">Этот метод выровняйте левый и верхний края окна до границ DWORD, что может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="9d723-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="9d723-112">Если окно имеет родителя, метод возвращает значение S ОК, \_ но выполняет выравнивание.</span><span class="sxs-lookup"><span data-stu-id="9d723-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d723-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9d723-113">Requirements</span></span>



| <span data-ttu-id="9d723-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9d723-114">Requirement</span></span> | <span data-ttu-id="9d723-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9d723-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d723-116">Header</span><span class="sxs-lookup"><span data-stu-id="9d723-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9d723-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d723-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d723-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d723-118">Library</span></span><br/> | <dl> <span data-ttu-id="9d723-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9d723-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d723-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d723-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d723-121">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="9d723-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 





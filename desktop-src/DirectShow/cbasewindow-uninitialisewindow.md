---
description: Метод Унинитиалисевиндов освобождает ресурсы окна.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Кбасевиндов. Унинитиалисевиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658044"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="ad3a4-103">Кбасевиндов. Унинитиалисевиндов, метод</span><span class="sxs-lookup"><span data-stu-id="ad3a4-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="ad3a4-104">`UninitialiseWindow`Метод освобождает ресурсы окна.</span><span class="sxs-lookup"><span data-stu-id="ad3a4-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad3a4-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="ad3a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad3a4-106">Parameters</span></span>

<span data-ttu-id="ad3a4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ad3a4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad3a4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad3a4-108">Return value</span></span>

<span data-ttu-id="ad3a4-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ad3a4-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad3a4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad3a4-110">Remarks</span></span>

<span data-ttu-id="ad3a4-111">Этот метод освобождает ресурсы, которые были получены методом [**кбасевиндов:: инитиалисевиндов**](cbasewindow-initialisewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="ad3a4-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="ad3a4-112">Метод [**кбасевиндов::D оневисвиндов**](cbasewindow-donewithwindow.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="ad3a4-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3a4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ad3a4-113">Requirements</span></span>



| <span data-ttu-id="ad3a4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ad3a4-114">Requirement</span></span> | <span data-ttu-id="ad3a4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ad3a4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3a4-116">Header</span><span class="sxs-lookup"><span data-stu-id="ad3a4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad3a4-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad3a4-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad3a4-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad3a4-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad3a4-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ad3a4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad3a4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad3a4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3a4-121">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="ad3a4-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 





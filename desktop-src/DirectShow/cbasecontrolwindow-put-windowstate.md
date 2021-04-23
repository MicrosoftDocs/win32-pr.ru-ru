---
description: Метод размещения \_ WindowState задает состояние окна.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Метод CBaseControlWindow.put_WindowState (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658063"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="c3fca-103">Кбасеконтролвиндов. размещение \_ метода WindowState</span><span class="sxs-lookup"><span data-stu-id="c3fca-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="c3fca-104">`put_WindowState`Метод задает состояние окна.</span><span class="sxs-lookup"><span data-stu-id="c3fca-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3fca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3fca-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="c3fca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3fca-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="c3fca-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="c3fca-108">Новое состояние окна.</span><span class="sxs-lookup"><span data-stu-id="c3fca-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3fca-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3fca-109">Return value</span></span>

<span data-ttu-id="c3fca-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3fca-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3fca-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3fca-111">Remarks</span></span>

<span data-ttu-id="c3fca-112">Эта функция-член принимает те же параметры, что и функция Microsoft Win32 **ShowWindow** (например, WS \_ шовнормал, WS \_ шовминноактивате и WS \_ шовмаксимизед).</span><span class="sxs-lookup"><span data-stu-id="c3fca-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3fca-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c3fca-113">Requirements</span></span>



| <span data-ttu-id="c3fca-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c3fca-114">Requirement</span></span> | <span data-ttu-id="c3fca-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c3fca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3fca-116">Header</span><span class="sxs-lookup"><span data-stu-id="c3fca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c3fca-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3fca-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3fca-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3fca-118">Library</span></span><br/> | <dl> <span data-ttu-id="c3fca-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c3fca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3fca-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3fca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3fca-121">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="c3fca-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





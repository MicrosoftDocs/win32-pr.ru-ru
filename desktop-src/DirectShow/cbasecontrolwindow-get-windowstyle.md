---
description: Метод Get \_ WindowStyle извлекает стандартные стили окна.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Метод CBaseControlWindow.get_WindowStyle (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657925"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="4a185-103">Кбасеконтролвиндов. Get \_ WindowStyle, метод</span><span class="sxs-lookup"><span data-stu-id="4a185-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="4a185-104">`get_WindowStyle`Метод получает стандартные стили окна.</span><span class="sxs-lookup"><span data-stu-id="4a185-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a185-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a185-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="4a185-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a185-107">*пвиндовстиле*</span><span class="sxs-lookup"><span data-stu-id="4a185-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="4a185-108">Указатель на стили окна.</span><span class="sxs-lookup"><span data-stu-id="4a185-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a185-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a185-109">Return value</span></span>

<span data-ttu-id="4a185-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a185-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a185-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a185-111">Remarks</span></span>

<span data-ttu-id="4a185-112">Эта функция – член возвращает стандартные стили окон, такие как WS \_ Child и WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="4a185-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="4a185-113">Он вызывает функцию члена [**кбасеконтролвиндов::D ожетвиндовстиле**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="4a185-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a185-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4a185-114">Requirements</span></span>



| <span data-ttu-id="4a185-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4a185-115">Requirement</span></span> | <span data-ttu-id="4a185-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a185-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a185-117">Header</span><span class="sxs-lookup"><span data-stu-id="4a185-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4a185-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a185-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a185-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a185-119">Library</span></span><br/> | <dl> <span data-ttu-id="4a185-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4a185-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a185-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a185-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a185-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="4a185-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





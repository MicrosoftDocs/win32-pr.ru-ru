---
description: Метод Дожетвиндовстиле извлекает текущие стандартные или расширенные стили окна.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Кбасеконтролвиндов. Дожетвиндовстиле, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668519"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="d7c00-103">Кбасеконтролвиндов. Дожетвиндовстиле, метод</span><span class="sxs-lookup"><span data-stu-id="d7c00-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="d7c00-104">`DoGetWindowStyle`Метод извлекает текущие стандартные или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="d7c00-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c00-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7c00-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="d7c00-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7c00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c00-107">*пстиле*</span><span class="sxs-lookup"><span data-stu-id="d7c00-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c00-108">Указатель на переменную, которая получает сведения о стиле.</span><span class="sxs-lookup"><span data-stu-id="d7c00-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="d7c00-109">*виндовлонг*</span><span class="sxs-lookup"><span data-stu-id="d7c00-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="d7c00-110">Значение, указывающее, какие стили следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="d7c00-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="d7c00-111">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="d7c00-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="d7c00-112">\_стиль ГВЛ</span><span class="sxs-lookup"><span data-stu-id="d7c00-112">GWL\_STYLE</span></span>   | <span data-ttu-id="d7c00-113">Получение стилей окна.</span><span class="sxs-lookup"><span data-stu-id="d7c00-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="d7c00-114">ГВЛ \_ операторе EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="d7c00-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="d7c00-115">Получение расширенных стилей окна.</span><span class="sxs-lookup"><span data-stu-id="d7c00-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c00-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7c00-116">Return value</span></span>

<span data-ttu-id="d7c00-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7c00-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7c00-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7c00-118">Remarks</span></span>

<span data-ttu-id="d7c00-119">Эта функция члена вызывает функцию Win32 **жетвиндовлонг** для получения стиля окна.</span><span class="sxs-lookup"><span data-stu-id="d7c00-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="d7c00-120">Он вызывается функциями-членами [**кбасеконтролвиндов:: Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) и [**кбасеконтролвиндов:: Get \_ виндовстиликс**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="d7c00-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c00-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d7c00-121">Requirements</span></span>



| <span data-ttu-id="d7c00-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d7c00-122">Requirement</span></span> | <span data-ttu-id="d7c00-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d7c00-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c00-124">Header</span><span class="sxs-lookup"><span data-stu-id="d7c00-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c00-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c00-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d7c00-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7c00-126">Library</span></span><br/> | <dl> <span data-ttu-id="d7c00-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c00-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c00-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7c00-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c00-129">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="d7c00-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





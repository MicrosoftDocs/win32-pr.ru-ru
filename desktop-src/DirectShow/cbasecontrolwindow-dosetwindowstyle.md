---
description: Метод Досетвиндовстиле изменяет стандартные или расширенные стили окна.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Кбасеконтролвиндов. Досетвиндовстиле, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656980"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="2685e-103">Кбасеконтролвиндов. Досетвиндовстиле, метод</span><span class="sxs-lookup"><span data-stu-id="2685e-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="2685e-104">`DoSetWindowStyle`Метод изменяет стандартные или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="2685e-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="2685e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2685e-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="2685e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2685e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2685e-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="2685e-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="2685e-108">Соответствующие стили окна.</span><span class="sxs-lookup"><span data-stu-id="2685e-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="2685e-109">*виндовлонг*</span><span class="sxs-lookup"><span data-stu-id="2685e-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="2685e-110">Значение, указывающее, какие стили задаются.</span><span class="sxs-lookup"><span data-stu-id="2685e-110">Value specifying which styles to set.</span></span> <span data-ttu-id="2685e-111">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="2685e-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="2685e-112">\_стиль ГВЛ</span><span class="sxs-lookup"><span data-stu-id="2685e-112">GWL\_STYLE</span></span>   | <span data-ttu-id="2685e-113">Получение стилей окна.</span><span class="sxs-lookup"><span data-stu-id="2685e-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="2685e-114">ГВЛ \_ операторе EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="2685e-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="2685e-115">Получение расширенных стилей окна.</span><span class="sxs-lookup"><span data-stu-id="2685e-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2685e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2685e-116">Return value</span></span>

<span data-ttu-id="2685e-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2685e-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2685e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2685e-118">Remarks</span></span>

<span data-ttu-id="2685e-119">Эта функция члена вызывает функцию Win32 **SetWindowLong** для задания стиля окна, а затем повторно отображает окно в текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="2685e-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="2685e-120">Эта функция-член вызывается с помощью функций-членов [**кбасеконтролвиндов::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) и [**кбасеконтролвиндов::p UT \_ виндовстиликс**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="2685e-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2685e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2685e-121">Requirements</span></span>



| <span data-ttu-id="2685e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2685e-122">Requirement</span></span> | <span data-ttu-id="2685e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2685e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2685e-124">Header</span><span class="sxs-lookup"><span data-stu-id="2685e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2685e-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2685e-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2685e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2685e-126">Library</span></span><br/> | <dl> <span data-ttu-id="2685e-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2685e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2685e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2685e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2685e-129">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="2685e-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909822"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="eb388-103">Кбасеконтролвиндов. Дожетвиндовстиле, метод</span><span class="sxs-lookup"><span data-stu-id="eb388-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="eb388-104">`DoGetWindowStyle`Метод извлекает текущие стандартные или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="eb388-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb388-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb388-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="eb388-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb388-107">*пстиле*</span><span class="sxs-lookup"><span data-stu-id="eb388-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="eb388-108">Указатель на переменную, которая получает сведения о стиле.</span><span class="sxs-lookup"><span data-stu-id="eb388-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="eb388-109">*виндовлонг*</span><span class="sxs-lookup"><span data-stu-id="eb388-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="eb388-110">Значение, указывающее, какие стили следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="eb388-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="eb388-111">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="eb388-111">Must be one of the following:</span></span>



| <span data-ttu-id="eb388-112">Метка</span><span class="sxs-lookup"><span data-stu-id="eb388-112">Label</span></span> | <span data-ttu-id="eb388-113">Значение</span><span class="sxs-lookup"><span data-stu-id="eb388-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="eb388-114">\_стиль ГВЛ</span><span class="sxs-lookup"><span data-stu-id="eb388-114">GWL\_STYLE</span></span>   | <span data-ttu-id="eb388-115">Получение стилей окна.</span><span class="sxs-lookup"><span data-stu-id="eb388-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="eb388-116">ГВЛ \_ операторе EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="eb388-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="eb388-117">Получение расширенных стилей окна.</span><span class="sxs-lookup"><span data-stu-id="eb388-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb388-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb388-118">Return value</span></span>

<span data-ttu-id="eb388-119">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb388-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb388-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb388-120">Remarks</span></span>

<span data-ttu-id="eb388-121">Эта функция члена вызывает функцию Win32 **жетвиндовлонг** для получения стиля окна.</span><span class="sxs-lookup"><span data-stu-id="eb388-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="eb388-122">Он вызывается функциями-членами [**кбасеконтролвиндов:: Get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) и [**кбасеконтролвиндов:: Get \_ виндовстиликс**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="eb388-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb388-123">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="eb388-123">Requirements</span></span>



| <span data-ttu-id="eb388-124">Требование</span><span class="sxs-lookup"><span data-stu-id="eb388-124">Requirement</span></span> | <span data-ttu-id="eb388-125">Значение</span><span class="sxs-lookup"><span data-stu-id="eb388-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb388-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="eb388-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eb388-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb388-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb388-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb388-128">Library</span></span><br/> | <dl> <span data-ttu-id="eb388-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="eb388-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb388-130">См. также</span><span class="sxs-lookup"><span data-stu-id="eb388-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb388-131">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="eb388-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





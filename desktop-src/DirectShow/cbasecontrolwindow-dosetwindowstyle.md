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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909812"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="7c982-103">Кбасеконтролвиндов. Досетвиндовстиле, метод</span><span class="sxs-lookup"><span data-stu-id="7c982-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="7c982-104">`DoSetWindowStyle`Метод изменяет стандартные или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="7c982-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c982-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c982-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="7c982-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c982-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c982-107">*Стиль*</span><span class="sxs-lookup"><span data-stu-id="7c982-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="7c982-108">Соответствующие стили окна.</span><span class="sxs-lookup"><span data-stu-id="7c982-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="7c982-109">*виндовлонг*</span><span class="sxs-lookup"><span data-stu-id="7c982-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="7c982-110">Значение, указывающее, какие стили задаются.</span><span class="sxs-lookup"><span data-stu-id="7c982-110">Value specifying which styles to set.</span></span> <span data-ttu-id="7c982-111">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="7c982-111">Must be one of the following:</span></span>



| <span data-ttu-id="7c982-112">Метка</span><span class="sxs-lookup"><span data-stu-id="7c982-112">Label</span></span> | <span data-ttu-id="7c982-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7c982-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="7c982-114">\_стиль ГВЛ</span><span class="sxs-lookup"><span data-stu-id="7c982-114">GWL\_STYLE</span></span>   | <span data-ttu-id="7c982-115">Получение стилей окна.</span><span class="sxs-lookup"><span data-stu-id="7c982-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="7c982-116">ГВЛ \_ операторе EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="7c982-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="7c982-117">Получение расширенных стилей окна.</span><span class="sxs-lookup"><span data-stu-id="7c982-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c982-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c982-118">Return value</span></span>

<span data-ttu-id="7c982-119">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c982-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c982-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c982-120">Remarks</span></span>

<span data-ttu-id="7c982-121">Эта функция члена вызывает функцию Win32 **SetWindowLong** для задания стиля окна, а затем повторно отображает окно в текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="7c982-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="7c982-122">Эта функция-член вызывается с помощью функций-членов [**кбасеконтролвиндов::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) и [**кбасеконтролвиндов::p UT \_ виндовстиликс**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="7c982-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c982-123">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="7c982-123">Requirements</span></span>



| <span data-ttu-id="7c982-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7c982-124">Requirement</span></span> | <span data-ttu-id="7c982-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7c982-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c982-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7c982-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c982-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c982-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c982-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c982-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c982-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c982-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c982-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7c982-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c982-131">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="7c982-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





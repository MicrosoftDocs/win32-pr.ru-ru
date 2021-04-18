---
description: Метод Комплетеконнект уведомляет окно о том, что закреплен входной ПИН-код модуля подготовки отчетов подключен.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Кбасевиндов. Комплетеконнект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674997"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="adcdc-103">Кбасевиндов. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="adcdc-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="adcdc-104">`CompleteConnect`Метод уведомляет окно о том, что закреплен входной ПИН-код модуля подготовки отчетов подключен.</span><span class="sxs-lookup"><span data-stu-id="adcdc-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="adcdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adcdc-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="adcdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adcdc-106">Parameters</span></span>

<span data-ttu-id="adcdc-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="adcdc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="adcdc-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adcdc-108">Return value</span></span>

<span data-ttu-id="adcdc-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="adcdc-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="adcdc-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adcdc-110">Remarks</span></span>

<span data-ttu-id="adcdc-111">Этот метод сбрасывает флаг активации окна ([**кбасевиндов:: m \_ бактиватед**](cbasewindow-m-bactivated.md)) в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="adcdc-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="adcdc-112">Когда модуль подготовки видео завершает соединение с закреплением, он может вызвать метод [**кбасевиндов:: активатевиндов**](cbasewindow-activatewindow.md) , чтобы задать размер и расположение окна.</span><span class="sxs-lookup"><span data-stu-id="adcdc-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="adcdc-113">Чтобы принудительно выполнить **активатевиндов** для повторного вычисления этих атрибутов, сначала вызовите `CompleteConnect` метод.</span><span class="sxs-lookup"><span data-stu-id="adcdc-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="adcdc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="adcdc-114">Requirements</span></span>



| <span data-ttu-id="adcdc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="adcdc-115">Requirement</span></span> | <span data-ttu-id="adcdc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="adcdc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adcdc-117">Header</span><span class="sxs-lookup"><span data-stu-id="adcdc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="adcdc-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adcdc-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adcdc-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="adcdc-119">Library</span></span><br/> | <dl> <span data-ttu-id="adcdc-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="adcdc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adcdc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adcdc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcdc-122">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="adcdc-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 





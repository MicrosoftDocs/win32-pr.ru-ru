---
description: Метод Исаутошовенаблед извлекает сведения о том, отображается ли видеоокно автоматически при приостановке или запуске фильтра подготовки отчетов.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Кбасеконтролвиндов. Исаутошовенаблед, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657459"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="e7e33-103">Кбасеконтролвиндов. Исаутошовенаблед, метод</span><span class="sxs-lookup"><span data-stu-id="e7e33-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="e7e33-104">`IsAutoShowEnabled`Метод получает сведения о том, отображается ли окно видео автоматически при приостановке или запуске фильтра подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="e7e33-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e33-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="e7e33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7e33-106">Parameters</span></span>

<span data-ttu-id="e7e33-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e7e33-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7e33-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7e33-108">Return value</span></span>

<span data-ttu-id="e7e33-109">Возвращает **значение true** , если элемент **m \_ баутошов** имеет значение 1 или **false** , если он имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e7e33-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e33-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7e33-110">Remarks</span></span>

<span data-ttu-id="e7e33-111">Если элемент **m \_ баутошов** имеет значение 1 в скрытом окне видео, окно становится видимым при приостановке или запуске фильтра.</span><span class="sxs-lookup"><span data-stu-id="e7e33-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="e7e33-112">Если для этого элемента задано значение 0, окно будет отображаться только при использовании функции-члена [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="e7e33-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="e7e33-113">Эта функция члена получает параметр **\_ баутошов элемента m** и имеет тот же результат, что и использование метода [**ивидеовиндов:: \_ Get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="e7e33-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e33-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e33-114">Requirements</span></span>



| <span data-ttu-id="e7e33-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e33-115">Requirement</span></span> | <span data-ttu-id="e7e33-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e33-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e33-117">Header</span><span class="sxs-lookup"><span data-stu-id="e7e33-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e7e33-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7e33-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7e33-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7e33-119">Library</span></span><br/> | <dl> <span data-ttu-id="e7e33-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e7e33-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e33-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7e33-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e33-122">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="e7e33-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





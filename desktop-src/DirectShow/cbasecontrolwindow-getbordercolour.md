---
description: Метод Жетбордерколаур извлекает текущий цвет границы окна, m \_ бордерколаур.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Кбасеконтролвиндов. Жетбордерколаур, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657461"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="7a304-103">Кбасеконтролвиндов. Жетбордерколаур, метод</span><span class="sxs-lookup"><span data-stu-id="7a304-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="7a304-104">`GetBorderColour`Метод получает текущий цвет границы окна, **m \_ бордерколаур**.</span><span class="sxs-lookup"><span data-stu-id="7a304-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a304-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a304-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="7a304-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a304-106">Parameters</span></span>

<span data-ttu-id="7a304-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7a304-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a304-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a304-108">Return value</span></span>

<span data-ttu-id="7a304-109">Возвращает цвет границы.</span><span class="sxs-lookup"><span data-stu-id="7a304-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a304-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a304-110">Remarks</span></span>

<span data-ttu-id="7a304-111">Приложение может задать конечный прямоугольник для вывода видео.</span><span class="sxs-lookup"><span data-stu-id="7a304-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="7a304-112">Этот прямоугольник должен относиться к клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="7a304-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="7a304-113">Если это сделано (по умолчанию всегда закрашивать все окно), то есть область, окружающая видео; то есть граница.</span><span class="sxs-lookup"><span data-stu-id="7a304-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="7a304-114">Цвет границы можно задать с помощью функции-члена [**кбасеконтролвиндов::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) .</span><span class="sxs-lookup"><span data-stu-id="7a304-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="7a304-115">Это свойство влияет на цвет границы.</span><span class="sxs-lookup"><span data-stu-id="7a304-115">This property affects the color of the border.</span></span> <span data-ttu-id="7a304-116">Используйте эту функцию-член вместо [**кбасеконтролвиндов:: Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), если только вы не вызываете это внешне через метод [**ивидеовиндов:: Get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .</span><span class="sxs-lookup"><span data-stu-id="7a304-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a304-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7a304-117">Requirements</span></span>



| <span data-ttu-id="7a304-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7a304-118">Requirement</span></span> | <span data-ttu-id="7a304-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7a304-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a304-120">Header</span><span class="sxs-lookup"><span data-stu-id="7a304-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7a304-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a304-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a304-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a304-122">Library</span></span><br/> | <dl> <span data-ttu-id="7a304-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7a304-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a304-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a304-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a304-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="7a304-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





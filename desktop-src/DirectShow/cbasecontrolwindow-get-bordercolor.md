---
description: Метод Get \_ BorderColor извлекает текущий цвет границы.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Метод CBaseControlWindow.get_BorderColor (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665281"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="ac8c3-103">Кбасеконтролвиндов. Get \_ BorderColor, метод</span><span class="sxs-lookup"><span data-stu-id="ac8c3-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="ac8c3-104">`get_BorderColor`Метод получает текущий цвет границы.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac8c3-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="ac8c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac8c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac8c3-107">*Цвет*</span><span class="sxs-lookup"><span data-stu-id="ac8c3-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="ac8c3-108">Указатель на текущий цвет границы.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac8c3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac8c3-109">Return value</span></span>

<span data-ttu-id="ac8c3-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac8c3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac8c3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac8c3-111">Remarks</span></span>

<span data-ttu-id="ac8c3-112">Приложение может задать конечный прямоугольник, в котором должно отображаться видео.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="ac8c3-113">Этот прямоугольник отсчитывается относительно клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="ac8c3-114">Если это сделано (по умолчанию всегда закрашивать все окно), то вокруг видео отображается граница.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="ac8c3-115">Это свойство влияет на цвет, используемый границей.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-115">This property affects the color used by the border.</span></span> <span data-ttu-id="ac8c3-116">Хотя параметр указан как тип **Long** , он фактически является значением **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="ac8c3-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="ac8c3-117">Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="ac8c3-118">Вызовите функцию члена [**кбасеконтролвиндов:: жетбордерколаур**](cbasecontrolwindow-getbordercolour.md) , чтобы получить это свойство, если не вызывается из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="ac8c3-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac8c3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ac8c3-119">Requirements</span></span>



| <span data-ttu-id="ac8c3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ac8c3-120">Requirement</span></span> | <span data-ttu-id="ac8c3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ac8c3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8c3-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac8c3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ac8c3-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac8c3-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ac8c3-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac8c3-124">Library</span></span><br/> | <dl> <span data-ttu-id="ac8c3-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ac8c3-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac8c3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac8c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8c3-127">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="ac8c3-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





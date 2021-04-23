---
description: Метод размещения \_ Top задает координату верхнего окна.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: Метод CBaseControlWindow.put_Top (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdbce19c3caf4129b1f224a740b27209b855a1f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658068"
---
# <a name="cbasecontrolwindowput_top-method"></a><span data-ttu-id="42a0a-103">Метод Кбасеконтролвиндов. Where \_ Top</span><span class="sxs-lookup"><span data-stu-id="42a0a-103">CBaseControlWindow.put\_Top method</span></span>

<span data-ttu-id="42a0a-104">`put_Top`Метод задает координату верхнего окна.</span><span class="sxs-lookup"><span data-stu-id="42a0a-104">The `put_Top` method sets the top window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a0a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42a0a-105">Syntax</span></span>


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a><span data-ttu-id="42a0a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42a0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a0a-107">*Top*</span><span class="sxs-lookup"><span data-stu-id="42a0a-107">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="42a0a-108">Новая Верхняя координата (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="42a0a-108">New top coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a0a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42a0a-109">Return value</span></span>

<span data-ttu-id="42a0a-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42a0a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a0a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42a0a-111">Remarks</span></span>

<span data-ttu-id="42a0a-112">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="42a0a-112">The window has a position on the desktop.</span></span> <span data-ttu-id="42a0a-113">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="42a0a-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="42a0a-114">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="42a0a-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="42a0a-115">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="42a0a-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="42a0a-116">Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="42a0a-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="42a0a-117">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="42a0a-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a0a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="42a0a-118">Requirements</span></span>



| <span data-ttu-id="42a0a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="42a0a-119">Requirement</span></span> | <span data-ttu-id="42a0a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="42a0a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a0a-121">Header</span><span class="sxs-lookup"><span data-stu-id="42a0a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="42a0a-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42a0a-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42a0a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42a0a-123">Library</span></span><br/> | <dl> <span data-ttu-id="42a0a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="42a0a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a0a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42a0a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a0a-126">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="42a0a-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





---
description: Метод размещения \_ Left задает левую координату для окна.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Метод CBaseControlWindow.put_Left (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657869"
---
# <a name="cbasecontrolwindowput_left-method"></a><span data-ttu-id="85957-103">Кбасеконтролвиндов. размещение \_ Left, метод</span><span class="sxs-lookup"><span data-stu-id="85957-103">CBaseControlWindow.put\_Left method</span></span>

<span data-ttu-id="85957-104">`put_Left`Метод задает левую координату окна.</span><span class="sxs-lookup"><span data-stu-id="85957-104">The `put_Left` method sets the left coordinate for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="85957-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85957-105">Syntax</span></span>


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a><span data-ttu-id="85957-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85957-107">*Слева*</span><span class="sxs-lookup"><span data-stu-id="85957-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="85957-108">Новая левая координата (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="85957-108">New left coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85957-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85957-109">Return value</span></span>

<span data-ttu-id="85957-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85957-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85957-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85957-111">Remarks</span></span>

<span data-ttu-id="85957-112">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="85957-112">The window has a position on the desktop.</span></span> <span data-ttu-id="85957-113">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="85957-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="85957-114">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="85957-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="85957-115">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="85957-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="85957-116">Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="85957-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="85957-117">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="85957-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="85957-118">Требования</span><span class="sxs-lookup"><span data-stu-id="85957-118">Requirements</span></span>



| <span data-ttu-id="85957-119">Требование</span><span class="sxs-lookup"><span data-stu-id="85957-119">Requirement</span></span> | <span data-ttu-id="85957-120">Значение</span><span class="sxs-lookup"><span data-stu-id="85957-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85957-121">Header</span><span class="sxs-lookup"><span data-stu-id="85957-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85957-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85957-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85957-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85957-123">Library</span></span><br/> | <dl> <span data-ttu-id="85957-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="85957-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85957-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85957-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85957-126">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="85957-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





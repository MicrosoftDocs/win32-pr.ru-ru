---
description: Метод размещения \_ ширины задает ширину окна.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: Метод CBaseControlWindow.put_Width (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658064"
---
# <a name="cbasecontrolwindowput_width-method"></a><span data-ttu-id="a360a-103">Кбасеконтролвиндов. размещение \_ метода Width</span><span class="sxs-lookup"><span data-stu-id="a360a-103">CBaseControlWindow.put\_Width method</span></span>

<span data-ttu-id="a360a-104">`put_Width`Метод задает ширину окна.</span><span class="sxs-lookup"><span data-stu-id="a360a-104">The `put_Width` method sets the window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="a360a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a360a-105">Syntax</span></span>


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a><span data-ttu-id="a360a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a360a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a360a-107">*Width*</span><span class="sxs-lookup"><span data-stu-id="a360a-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="a360a-108">Новая ширина окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a360a-108">New window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a360a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a360a-109">Return value</span></span>

<span data-ttu-id="a360a-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a360a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a360a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a360a-111">Remarks</span></span>

<span data-ttu-id="a360a-112">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="a360a-112">The window has a position on the desktop.</span></span> <span data-ttu-id="a360a-113">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="a360a-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="a360a-114">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a360a-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="a360a-115">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="a360a-115">All coordinates are expressed in pixels and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="a360a-116">Установка координат Left или Top приводит к перемещению окна влево или вверх соответственно. Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="a360a-116">Setting the left or top coordinates moves the window left or up respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="a360a-117">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="a360a-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="a360a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a360a-118">Requirements</span></span>



| <span data-ttu-id="a360a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a360a-119">Requirement</span></span> | <span data-ttu-id="a360a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a360a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a360a-121">Header</span><span class="sxs-lookup"><span data-stu-id="a360a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a360a-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a360a-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a360a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a360a-123">Library</span></span><br/> | <dl> <span data-ttu-id="a360a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a360a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a360a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a360a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a360a-126">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="a360a-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





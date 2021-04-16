---
description: Метод Get \_ Top Получает координату верхнего окна.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: Метод CBaseControlWindow.get_Top (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9861d930cdb2d93e5e0b73ffad625885c082cb6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657928"
---
# <a name="cbasecontrolwindowget_top-method"></a><span data-ttu-id="9f11e-103">Кбасеконтролвиндов. Get, \_ метод Top</span><span class="sxs-lookup"><span data-stu-id="9f11e-103">CBaseControlWindow.get\_Top method</span></span>

<span data-ttu-id="9f11e-104">`get_Top`Метод получает координату верхнего окна.</span><span class="sxs-lookup"><span data-stu-id="9f11e-104">The `get_Top` method retrieves the top window coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f11e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f11e-105">Syntax</span></span>


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a><span data-ttu-id="9f11e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f11e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f11e-107">*птоп*</span><span class="sxs-lookup"><span data-stu-id="9f11e-107">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="9f11e-108">Указатель на верхнюю координату (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="9f11e-108">Pointer to the top coordinate, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f11e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f11e-109">Return value</span></span>

<span data-ttu-id="9f11e-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f11e-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f11e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f11e-111">Remarks</span></span>

<span data-ttu-id="9f11e-112">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="9f11e-112">The window has a position on the desktop.</span></span> <span data-ttu-id="9f11e-113">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="9f11e-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="9f11e-114">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9f11e-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="9f11e-115">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="9f11e-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="9f11e-116">Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="9f11e-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="9f11e-117">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="9f11e-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f11e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9f11e-118">Requirements</span></span>



| <span data-ttu-id="9f11e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9f11e-119">Requirement</span></span> | <span data-ttu-id="9f11e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9f11e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f11e-121">Header</span><span class="sxs-lookup"><span data-stu-id="9f11e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9f11e-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f11e-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f11e-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f11e-123">Library</span></span><br/> | <dl> <span data-ttu-id="9f11e-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9f11e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f11e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f11e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f11e-126">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="9f11e-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





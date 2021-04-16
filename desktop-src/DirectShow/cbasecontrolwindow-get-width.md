---
description: Метод Get \_ Width извлекает текущую ширину окна.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Метод CBaseControlWindow.get_Width (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657926"
---
# <a name="cbasecontrolwindowget_width-method"></a><span data-ttu-id="7f2f6-103">Кбасеконтролвиндов. Get, \_ метод Width</span><span class="sxs-lookup"><span data-stu-id="7f2f6-103">CBaseControlWindow.get\_Width method</span></span>

<span data-ttu-id="7f2f6-104">`get_Width`Метод получает текущую ширину окна.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-104">The `get_Width` method retrieves the current window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f2f6-105">Syntax</span></span>


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a><span data-ttu-id="7f2f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f2f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f2f6-107">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="7f2f6-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="7f2f6-108">Указатель на ширину окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-108">Pointer to the window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f2f6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f2f6-109">Return value</span></span>

<span data-ttu-id="7f2f6-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f2f6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2f6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f2f6-111">Remarks</span></span>

<span data-ttu-id="7f2f6-112">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-112">The window has a position on the desktop.</span></span> <span data-ttu-id="7f2f6-113">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="7f2f6-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="7f2f6-114">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="7f2f6-115">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-115">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="7f2f6-116">Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-116">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="7f2f6-117">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="7f2f6-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2f6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7f2f6-118">Requirements</span></span>



| <span data-ttu-id="7f2f6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7f2f6-119">Requirement</span></span> | <span data-ttu-id="7f2f6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7f2f6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2f6-121">Header</span><span class="sxs-lookup"><span data-stu-id="7f2f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7f2f6-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f6-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f2f6-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f2f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="7f2f6-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2f6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f2f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2f6-126">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="7f2f6-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





---
description: Метод получения \_ высоты извлекает текущую высоту окна.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Метод CBaseControlWindow.get_Height (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657168"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="5335d-103">Кбасеконтролвиндов. Get, \_ метод Height</span><span class="sxs-lookup"><span data-stu-id="5335d-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="5335d-104">`get_Height`Метод получает текущую высоту окна.</span><span class="sxs-lookup"><span data-stu-id="5335d-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="5335d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5335d-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5335d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5335d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5335d-107">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="5335d-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5335d-108">Указатель на текущую высоту окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5335d-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5335d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5335d-109">Return value</span></span>

<span data-ttu-id="5335d-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5335d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5335d-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5335d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5335d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5335d-112">Remarks</span></span>

<span data-ttu-id="5335d-113">Окно располагается на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="5335d-113">The window has a position on the desktop.</span></span> <span data-ttu-id="5335d-114">Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу).</span><span class="sxs-lookup"><span data-stu-id="5335d-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="5335d-115">Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5335d-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="5335d-116">Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.</span><span class="sxs-lookup"><span data-stu-id="5335d-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="5335d-117">Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна.</span><span class="sxs-lookup"><span data-stu-id="5335d-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="5335d-118">Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.</span><span class="sxs-lookup"><span data-stu-id="5335d-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="5335d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5335d-119">Requirements</span></span>



| <span data-ttu-id="5335d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5335d-120">Requirement</span></span> | <span data-ttu-id="5335d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5335d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5335d-122">Header</span><span class="sxs-lookup"><span data-stu-id="5335d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5335d-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5335d-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5335d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5335d-124">Library</span></span><br/> | <dl> <span data-ttu-id="5335d-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5335d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5335d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5335d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5335d-127">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="5335d-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





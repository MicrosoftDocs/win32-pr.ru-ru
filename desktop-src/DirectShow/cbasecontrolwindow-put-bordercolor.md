---
description: Метод «разместить \_ BorderColor» изменяет цвет границы.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Метод CBaseControlWindow.put_BorderColor (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657350"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="314f0-103">Кбасеконтролвиндов. размещение \_ BorderColor, метод</span><span class="sxs-lookup"><span data-stu-id="314f0-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="314f0-104">`put_BorderColor`Метод изменяет цвет границы.</span><span class="sxs-lookup"><span data-stu-id="314f0-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="314f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="314f0-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="314f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="314f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314f0-107">*Цвет*</span><span class="sxs-lookup"><span data-stu-id="314f0-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="314f0-108">Новый цвет границы.</span><span class="sxs-lookup"><span data-stu-id="314f0-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314f0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="314f0-109">Return value</span></span>

<span data-ttu-id="314f0-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="314f0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="314f0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="314f0-111">Remarks</span></span>

<span data-ttu-id="314f0-112">Приложение может установить конечный прямоугольник, в котором должно отображаться видео.</span><span class="sxs-lookup"><span data-stu-id="314f0-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="314f0-113">Этот прямоугольник отсчитывается относительно клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="314f0-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="314f0-114">Если это сделано (по умолчанию всегда закрашивать все окно), то вокруг видео отображается граница.</span><span class="sxs-lookup"><span data-stu-id="314f0-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="314f0-115">Это свойство влияет на цвет, используемый границей.</span><span class="sxs-lookup"><span data-stu-id="314f0-115">This property affects the color used by the border.</span></span> <span data-ttu-id="314f0-116">Хотя параметр указан как тип **Long** , он фактически является значением **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="314f0-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="314f0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="314f0-117">Requirements</span></span>



| <span data-ttu-id="314f0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="314f0-118">Requirement</span></span> | <span data-ttu-id="314f0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="314f0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314f0-120">Header</span><span class="sxs-lookup"><span data-stu-id="314f0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="314f0-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="314f0-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="314f0-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="314f0-122">Library</span></span><br/> | <dl> <span data-ttu-id="314f0-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="314f0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314f0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="314f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314f0-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="314f0-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





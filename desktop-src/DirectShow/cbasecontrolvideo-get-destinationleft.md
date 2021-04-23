---
description: Метод Get \_ дестинатионлефт извлекает левую координату текущего прямоугольника назначения.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: Метод CBaseControlVideo.get_DestinationLeft (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f433d880fd7f568a173a91c533e0d07bf97e6443
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688767"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a><span data-ttu-id="b6be7-103">Кбасеконтролвидео. Get \_ дестинатионлефт, метод</span><span class="sxs-lookup"><span data-stu-id="b6be7-103">CBaseControlVideo.get\_DestinationLeft method</span></span>

<span data-ttu-id="b6be7-104">`get_DestinationLeft`Метод извлекает левую координату текущего прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="b6be7-104">The `get_DestinationLeft` method retrieves the left coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6be7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6be7-105">Syntax</span></span>


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a><span data-ttu-id="b6be7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6be7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6be7-107">*пдестинатионлефт*</span><span class="sxs-lookup"><span data-stu-id="b6be7-107">*pDestinationLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="b6be7-108">Указатель на левую координату прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="b6be7-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6be7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6be7-109">Return value</span></span>

<span data-ttu-id="b6be7-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="b6be7-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b6be7-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b6be7-111">Return code</span></span>                                                                                           | <span data-ttu-id="b6be7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b6be7-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6be7-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b6be7-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="b6be7-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b6be7-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b6be7-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="b6be7-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b6be7-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b6be7-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="b6be7-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="b6be7-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b6be7-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b6be7-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b6be7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6be7-121">Remarks</span></span>

<span data-ttu-id="b6be7-122">Эта функция члена реализует метод [**ибасиквидео:: Get \_ дестинатионлефт**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) .</span><span class="sxs-lookup"><span data-stu-id="b6be7-122">This member function implements the [**IBasicVideo::get\_DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) method.</span></span>

<span data-ttu-id="b6be7-123">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="b6be7-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b6be7-124">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="b6be7-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b6be7-125">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="b6be7-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b6be7-126">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="b6be7-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6be7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b6be7-127">Requirements</span></span>



| <span data-ttu-id="b6be7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b6be7-128">Requirement</span></span> | <span data-ttu-id="b6be7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b6be7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6be7-130">Header</span><span class="sxs-lookup"><span data-stu-id="b6be7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b6be7-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6be7-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6be7-132">Library</span></span><br/> | <dl> <span data-ttu-id="b6be7-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6be7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6be7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6be7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6be7-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="b6be7-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





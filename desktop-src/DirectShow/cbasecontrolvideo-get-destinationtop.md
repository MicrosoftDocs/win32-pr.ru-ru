---
description: Метод Get \_ дестинатионтоп извлекает верхнюю координату текущего прямоугольника назначения.
ms.assetid: 8d5c1361-18db-4ea1-a507-781397189630
title: Метод CBaseControlVideo.get_DestinationTop (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2c7d450c50b11186546a25ceebd317a308dd805
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657241"
---
# <a name="cbasecontrolvideoget_destinationtop-method"></a><span data-ttu-id="dc225-103">Кбасеконтролвидео. Get \_ дестинатионтоп, метод</span><span class="sxs-lookup"><span data-stu-id="dc225-103">CBaseControlVideo.get\_DestinationTop method</span></span>

<span data-ttu-id="dc225-104">`get_DestinationTop`Метод получает верхнюю координату текущего прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="dc225-104">The `get_DestinationTop` method retrieves the top coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc225-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc225-105">Syntax</span></span>


```C++
HRESULT get_DestinationTop(
   long *pDestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="dc225-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc225-107">*пдестинатионтоп*</span><span class="sxs-lookup"><span data-stu-id="dc225-107">*pDestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="dc225-108">Указатель на верхнюю координату прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="dc225-108">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc225-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc225-109">Return value</span></span>

<span data-ttu-id="dc225-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="dc225-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="dc225-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc225-111">Return code</span></span>                                                                                           | <span data-ttu-id="dc225-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dc225-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc225-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="dc225-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="dc225-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="dc225-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="dc225-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="dc225-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dc225-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dc225-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="dc225-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="dc225-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="dc225-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="dc225-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="dc225-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc225-121">Remarks</span></span>

<span data-ttu-id="dc225-122">Эта функция члена реализует метод [**ибасиквидео:: Get \_ дестинатионтоп**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) .</span><span class="sxs-lookup"><span data-stu-id="dc225-122">This member function implements the [**IBasicVideo::get\_DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) method.</span></span>

<span data-ttu-id="dc225-123">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="dc225-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="dc225-124">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="dc225-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="dc225-125">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="dc225-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="dc225-126">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="dc225-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc225-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dc225-127">Requirements</span></span>



| <span data-ttu-id="dc225-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dc225-128">Requirement</span></span> | <span data-ttu-id="dc225-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dc225-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc225-130">Header</span><span class="sxs-lookup"><span data-stu-id="dc225-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dc225-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc225-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc225-132">Library</span></span><br/> | <dl> <span data-ttu-id="dc225-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dc225-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc225-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc225-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc225-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="dc225-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





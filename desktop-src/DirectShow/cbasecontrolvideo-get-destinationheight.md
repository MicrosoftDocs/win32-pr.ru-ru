---
description: Метод Get \_ дестинатионхеигхт извлекает текущую высоту прямоугольника назначения.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: Метод CBaseControlVideo.get_DestinationHeight (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc4fc63e63adbc42b75ae9a24d1c47e7d985c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657242"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a><span data-ttu-id="2b712-103">Кбасеконтролвидео. Get \_ дестинатионхеигхт, метод</span><span class="sxs-lookup"><span data-stu-id="2b712-103">CBaseControlVideo.get\_DestinationHeight method</span></span>

<span data-ttu-id="2b712-104">`get_DestinationHeight`Метод извлекает текущую высоту прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="2b712-104">The `get_DestinationHeight` method retrieves the current destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b712-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b712-105">Syntax</span></span>


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="2b712-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b712-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b712-107">*пдестинатионхеигхт*</span><span class="sxs-lookup"><span data-stu-id="2b712-107">*pDestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="2b712-108">Указатель на целевую высоту.</span><span class="sxs-lookup"><span data-stu-id="2b712-108">Pointer to the destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b712-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b712-109">Return value</span></span>

<span data-ttu-id="2b712-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="2b712-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="2b712-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b712-111">Return code</span></span>                                                                                           | <span data-ttu-id="2b712-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2b712-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b712-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="2b712-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="2b712-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2b712-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="2b712-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="2b712-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2b712-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2b712-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="2b712-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="2b712-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="2b712-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2b712-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="2b712-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b712-121">Remarks</span></span>

<span data-ttu-id="2b712-122">Эта функция члена реализует метод [**ибасиквидео:: Get \_ дестинатионхеигхт**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) .</span><span class="sxs-lookup"><span data-stu-id="2b712-122">This member function implements the [**IBasicVideo::get\_DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) method.</span></span>

<span data-ttu-id="2b712-123">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="2b712-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="2b712-124">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. конечный прямоугольник влияет на то, где он будет воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="2b712-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where it will be played.</span></span> <span data-ttu-id="2b712-125">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="2b712-125">The destination rectangle is relative to the client area of the window that it is playing in.</span></span> <span data-ttu-id="2b712-126">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="2b712-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b712-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2b712-127">Requirements</span></span>



| <span data-ttu-id="2b712-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2b712-128">Requirement</span></span> | <span data-ttu-id="2b712-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2b712-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b712-130">Header</span><span class="sxs-lookup"><span data-stu-id="2b712-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2b712-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b712-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b712-132">Library</span></span><br/> | <dl> <span data-ttu-id="2b712-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2b712-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b712-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b712-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b712-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="2b712-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





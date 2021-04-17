---
description: Метод размещения \_ дестинатионтоп задает верхнюю координату целевого прямоугольника.
ms.assetid: d18996ac-85f2-4778-b0aa-1bc0c4d5f7d9
title: Метод CBaseControlVideo.put_DestinationTop (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c89e4693d424412a43869509e046a5023e76341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657533"
---
# <a name="cbasecontrolvideoput_destinationtop-method"></a><span data-ttu-id="fa6c0-103">Кбасеконтролвидео. размещение \_ метода дестинатионтоп</span><span class="sxs-lookup"><span data-stu-id="fa6c0-103">CBaseControlVideo.put\_DestinationTop method</span></span>

<span data-ttu-id="fa6c0-104">`put_DestinationTop`Метод задает верхнюю координату конечного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-104">The `put_DestinationTop` method sets the top coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa6c0-105">Syntax</span></span>


```C++
HRESULT put_DestinationTop(
   long DestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="fa6c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa6c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa6c0-107">*дестинатионтоп*</span><span class="sxs-lookup"><span data-stu-id="fa6c0-107">*DestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="fa6c0-108">Новая Верхняя координата прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-108">New top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa6c0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa6c0-109">Return value</span></span>

<span data-ttu-id="fa6c0-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="fa6c0-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fa6c0-111">Return code</span></span>                                                                                           | <span data-ttu-id="fa6c0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fa6c0-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa6c0-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="fa6c0-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="fa6c0-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="fa6c0-116">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="fa6c0-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="fa6c0-118">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fa6c0-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="fa6c0-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="fa6c0-121"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fa6c0-122">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa6c0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa6c0-123">Remarks</span></span>

<span data-ttu-id="fa6c0-124">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="fa6c0-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="fa6c0-125">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="fa6c0-126">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="fa6c0-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="fa6c0-127">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="fa6c0-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6c0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fa6c0-128">Requirements</span></span>



| <span data-ttu-id="fa6c0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fa6c0-129">Requirement</span></span> | <span data-ttu-id="fa6c0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fa6c0-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6c0-131">Header</span><span class="sxs-lookup"><span data-stu-id="fa6c0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fa6c0-132"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa6c0-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa6c0-133">Library</span></span><br/> | <dl> <span data-ttu-id="fa6c0-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fa6c0-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa6c0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa6c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6c0-136">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="fa6c0-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





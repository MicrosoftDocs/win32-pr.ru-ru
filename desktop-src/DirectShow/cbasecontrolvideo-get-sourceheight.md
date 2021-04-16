---
description: Метод Get \_ саурцехеигхт извлекает высоту текущего исходного прямоугольника.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Метод CBaseControlVideo.get_SourceHeight (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657239"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a><span data-ttu-id="4cfaa-103">Кбасеконтролвидео. Get \_ саурцехеигхт, метод</span><span class="sxs-lookup"><span data-stu-id="4cfaa-103">CBaseControlVideo.get\_SourceHeight method</span></span>

<span data-ttu-id="4cfaa-104">`get_SourceHeight`Метод получает высоту текущего исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-104">The `get_SourceHeight` method retrieves the height of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfaa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cfaa-105">Syntax</span></span>


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a><span data-ttu-id="4cfaa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cfaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfaa-107">*псаурцехеигхт*</span><span class="sxs-lookup"><span data-stu-id="4cfaa-107">*pSourceHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="4cfaa-108">Указатель на высоту исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-108">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfaa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cfaa-109">Return value</span></span>

<span data-ttu-id="4cfaa-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="4cfaa-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4cfaa-111">Return code</span></span>                                                                                           | <span data-ttu-id="4cfaa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4cfaa-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cfaa-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="4cfaa-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="4cfaa-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="4cfaa-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="4cfaa-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4cfaa-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="4cfaa-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="4cfaa-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="4cfaa-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cfaa-121">Remarks</span></span>

<span data-ttu-id="4cfaa-122">Эта функция члена реализует метод [**ибасиквидео:: Get \_ саурцехеигхт**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .</span><span class="sxs-lookup"><span data-stu-id="4cfaa-122">This member function implements the [**IBasicVideo::get\_SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) method.</span></span>

<span data-ttu-id="4cfaa-123">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="4cfaa-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="4cfaa-124">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="4cfaa-125">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="4cfaa-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="4cfaa-126">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="4cfaa-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfaa-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4cfaa-127">Requirements</span></span>



| <span data-ttu-id="4cfaa-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4cfaa-128">Requirement</span></span> | <span data-ttu-id="4cfaa-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4cfaa-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfaa-130">Header</span><span class="sxs-lookup"><span data-stu-id="4cfaa-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfaa-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cfaa-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4cfaa-132">Library</span></span><br/> | <dl> <span data-ttu-id="4cfaa-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4cfaa-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cfaa-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cfaa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfaa-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="4cfaa-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: Метод Get \_ саурцевидс извлекает ширину текущего исходного прямоугольника.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: Метод CBaseControlVideo.get_SourceWidth (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657236"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="c170c-103">Кбасеконтролвидео. Get \_ саурцевидс, метод</span><span class="sxs-lookup"><span data-stu-id="c170c-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="c170c-104">`get_SourceWidth`Метод получает ширину текущего исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="c170c-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c170c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c170c-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="c170c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c170c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c170c-107">*псаурцевидс*</span><span class="sxs-lookup"><span data-stu-id="c170c-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="c170c-108">Указатель на ширину текущего исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="c170c-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c170c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c170c-109">Return value</span></span>

<span data-ttu-id="c170c-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="c170c-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="c170c-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c170c-111">Return code</span></span>                                                                                           | <span data-ttu-id="c170c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c170c-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c170c-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="c170c-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="c170c-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="c170c-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c170c-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="c170c-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c170c-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c170c-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="c170c-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="c170c-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="c170c-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c170c-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="c170c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c170c-121">Remarks</span></span>

<span data-ttu-id="c170c-122">Эта функция члена реализует метод [**ибасиквидео:: Get \_ саурцевидс**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) .</span><span class="sxs-lookup"><span data-stu-id="c170c-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="c170c-123">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="c170c-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="c170c-124">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="c170c-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="c170c-125">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="c170c-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="c170c-126">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="c170c-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c170c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c170c-127">Requirements</span></span>



| <span data-ttu-id="c170c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c170c-128">Requirement</span></span> | <span data-ttu-id="c170c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c170c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c170c-130">Header</span><span class="sxs-lookup"><span data-stu-id="c170c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c170c-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c170c-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c170c-132">Library</span></span><br/> | <dl> <span data-ttu-id="c170c-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c170c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c170c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c170c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c170c-135">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="c170c-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





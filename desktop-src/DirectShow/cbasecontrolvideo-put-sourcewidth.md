---
description: Метод размещения \_ саурцевидс задает ширину исходного прямоугольника.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: Метод CBaseControlVideo.put_SourceWidth (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1576389a90db71ee6d371f6e68c44ea39117c05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665288"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a><span data-ttu-id="8027b-103">Кбасеконтролвидео. размещение \_ метода саурцевидс</span><span class="sxs-lookup"><span data-stu-id="8027b-103">CBaseControlVideo.put\_SourceWidth method</span></span>

<span data-ttu-id="8027b-104">`put_SourceWidth`Метод задает ширину исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="8027b-104">The `put_SourceWidth` method sets the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8027b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8027b-105">Syntax</span></span>


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="8027b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8027b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8027b-107">*саурцевидс*</span><span class="sxs-lookup"><span data-stu-id="8027b-107">*SourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="8027b-108">Новая ширина исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="8027b-108">New width of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8027b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8027b-109">Return value</span></span>

<span data-ttu-id="8027b-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="8027b-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="8027b-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8027b-111">Return code</span></span>                                                                                           | <span data-ttu-id="8027b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8027b-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8027b-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="8027b-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="8027b-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="8027b-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="8027b-116">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="8027b-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="8027b-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="8027b-118">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="8027b-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8027b-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="8027b-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8027b-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="8027b-121"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8027b-122">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="8027b-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8027b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8027b-123">Remarks</span></span>

<span data-ttu-id="8027b-124">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="8027b-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="8027b-125">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="8027b-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="8027b-126">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="8027b-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="8027b-127">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="8027b-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="8027b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8027b-128">Requirements</span></span>



| <span data-ttu-id="8027b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8027b-129">Requirement</span></span> | <span data-ttu-id="8027b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8027b-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8027b-131">Header</span><span class="sxs-lookup"><span data-stu-id="8027b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8027b-132"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8027b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8027b-133">Library</span></span><br/> | <dl> <span data-ttu-id="8027b-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8027b-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8027b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8027b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8027b-136">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="8027b-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





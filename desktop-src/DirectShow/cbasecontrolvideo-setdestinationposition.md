---
description: Метод Сетдестинатионпоситион задает прямоугольник назначения для видео.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Кбасеконтролвидео. Сетдестинатионпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669477"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a><span data-ttu-id="7f4bc-103">Кбасеконтролвидео. Сетдестинатионпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="7f4bc-103">CBaseControlVideo.SetDestinationPosition method</span></span>

<span data-ttu-id="7f4bc-104">`SetDestinationPosition`Метод задает прямоугольник назначения для видео.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-104">The `SetDestinationPosition` method sets the destination rectangle for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f4bc-105">Syntax</span></span>


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="7f4bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f4bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4bc-107">*Слева*</span><span class="sxs-lookup"><span data-stu-id="7f4bc-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="7f4bc-108">Новая левая координата.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="7f4bc-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="7f4bc-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="7f4bc-110">Новая Верхняя координата.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="7f4bc-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="7f4bc-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="7f4bc-112">Новая ширина.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="7f4bc-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="7f4bc-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="7f4bc-114">Новая высота.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4bc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f4bc-115">Return value</span></span>

<span data-ttu-id="7f4bc-116">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="7f4bc-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7f4bc-117">Return code</span></span>                                                                                           | <span data-ttu-id="7f4bc-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7f4bc-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f4bc-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="7f4bc-120">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="7f4bc-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="7f4bc-122">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="7f4bc-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="7f4bc-124">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="7f4bc-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="7f4bc-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="7f4bc-127"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7f4bc-128">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f4bc-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f4bc-129">Remarks</span></span>

<span data-ttu-id="7f4bc-130">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="7f4bc-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="7f4bc-131">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="7f4bc-132">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="7f4bc-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="7f4bc-133">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="7f4bc-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4bc-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7f4bc-134">Requirements</span></span>



| <span data-ttu-id="7f4bc-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7f4bc-135">Requirement</span></span> | <span data-ttu-id="7f4bc-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7f4bc-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4bc-137">Header</span><span class="sxs-lookup"><span data-stu-id="7f4bc-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7f4bc-138"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f4bc-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f4bc-139">Library</span></span><br/> | <dl> <span data-ttu-id="7f4bc-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4bc-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4bc-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f4bc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4bc-142">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="7f4bc-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





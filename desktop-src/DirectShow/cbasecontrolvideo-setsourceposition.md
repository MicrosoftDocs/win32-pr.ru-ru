---
description: Метод Сетсаурцепоситион задает новую исходную точку для видео.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: Кбасеконтролвидео. Сетсаурцепоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658026"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="bf8b6-103">Кбасеконтролвидео. Сетсаурцепоситион, метод</span><span class="sxs-lookup"><span data-stu-id="bf8b6-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="bf8b6-104">`SetSourcePosition`Метод задает новую исходную точку для видео.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf8b6-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="bf8b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf8b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8b6-107">*Слева*</span><span class="sxs-lookup"><span data-stu-id="bf8b6-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8b6-108">Новая левая координата.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bf8b6-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="bf8b6-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8b6-110">Новая Верхняя координата.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bf8b6-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="bf8b6-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8b6-112">Новая ширина.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="bf8b6-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="bf8b6-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8b6-114">Новая высота.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8b6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf8b6-115">Return value</span></span>

<span data-ttu-id="bf8b6-116">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="bf8b6-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bf8b6-117">Return code</span></span>                                                                                           | <span data-ttu-id="bf8b6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="bf8b6-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf8b6-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="bf8b6-120">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="bf8b6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="bf8b6-122">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="bf8b6-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="bf8b6-124">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="bf8b6-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="bf8b6-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="bf8b6-127"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bf8b6-128">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf8b6-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf8b6-129">Remarks</span></span>

<span data-ttu-id="bf8b6-130">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="bf8b6-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="bf8b6-131">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="bf8b6-132">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="bf8b6-133">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="bf8b6-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8b6-134">Требования</span><span class="sxs-lookup"><span data-stu-id="bf8b6-134">Requirements</span></span>



| <span data-ttu-id="bf8b6-135">Требование</span><span class="sxs-lookup"><span data-stu-id="bf8b6-135">Requirement</span></span> | <span data-ttu-id="bf8b6-136">Значение</span><span class="sxs-lookup"><span data-stu-id="bf8b6-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8b6-137">Header</span><span class="sxs-lookup"><span data-stu-id="bf8b6-137">Header</span></span><br/>  | <dl> <span data-ttu-id="bf8b6-138"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf8b6-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf8b6-139">Library</span></span><br/> | <dl> <span data-ttu-id="bf8b6-140"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8b6-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf8b6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8b6-142">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





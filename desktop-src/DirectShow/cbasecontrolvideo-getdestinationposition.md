---
description: Метод Жетдестинатионпоситион извлекает прямоугольник назначения в рамках одной атомарной операции.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Кбасеконтролвидео. Жетдестинатионпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658129"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="7580d-103">Кбасеконтролвидео. Жетдестинатионпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="7580d-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="7580d-104">`GetDestinationPosition`Метод извлекает прямоугольник назначения в рамках одной атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="7580d-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7580d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7580d-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="7580d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7580d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7580d-107">*плефт*</span><span class="sxs-lookup"><span data-stu-id="7580d-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="7580d-108">Указатель на левую координату прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="7580d-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7580d-109">*птоп*</span><span class="sxs-lookup"><span data-stu-id="7580d-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="7580d-110">Указатель на верхнюю координату прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="7580d-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7580d-111">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="7580d-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="7580d-112">Указатель на ширину прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="7580d-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7580d-113">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="7580d-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="7580d-114">Указатель на высоту прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="7580d-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7580d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7580d-115">Return value</span></span>

<span data-ttu-id="7580d-116">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="7580d-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="7580d-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7580d-117">Return code</span></span>                                                                                           | <span data-ttu-id="7580d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7580d-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7580d-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="7580d-120">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="7580d-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="7580d-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="7580d-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="7580d-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="7580d-123"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7580d-124">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="7580d-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="7580d-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="7580d-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7580d-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="7580d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7580d-127">Remarks</span></span>

<span data-ttu-id="7580d-128">Эту функцию члена можно использовать вместо отдельных вызовов функций члена [**кбасеконтролвидео:: Get \_ дестинатионлефт**](cbasecontrolvideo-get-destinationleft.md), [**кбасеконтролвидео:: Get \_ дестинатионтоп**](cbasecontrolvideo-get-destinationtop.md), [**кбасеконтролвидео:: Get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)и [**CBaseControlVideo:: Get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) .</span><span class="sxs-lookup"><span data-stu-id="7580d-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="7580d-129">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="7580d-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="7580d-130">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="7580d-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="7580d-131">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="7580d-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="7580d-132">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="7580d-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="7580d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7580d-133">Requirements</span></span>



| <span data-ttu-id="7580d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7580d-134">Requirement</span></span> | <span data-ttu-id="7580d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7580d-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7580d-136">Header</span><span class="sxs-lookup"><span data-stu-id="7580d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7580d-137"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7580d-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7580d-138">Library</span></span><br/> | <dl> <span data-ttu-id="7580d-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7580d-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7580d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7580d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7580d-141">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="7580d-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





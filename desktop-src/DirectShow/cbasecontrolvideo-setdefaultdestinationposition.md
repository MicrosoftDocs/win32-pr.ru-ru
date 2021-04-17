---
description: Метод Сетдефаултдестинатионпоситион задает для модуля подготовки отчетов использование целевой точки назначения по умолчанию (обычно это все окно клиентской области).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Кбасеконтролвидео. Сетдефаултдестинатионпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665284"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="3057f-103">Кбасеконтролвидео. Сетдефаултдестинатионпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="3057f-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="3057f-104">`SetDefaultDestinationPosition`Метод задает для модуля подготовки отчетов значение, используемое по умолчанию (обычно это вся клиентская область окна).</span><span class="sxs-lookup"><span data-stu-id="3057f-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="3057f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3057f-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="3057f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3057f-106">Parameters</span></span>

<span data-ttu-id="3057f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3057f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3057f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3057f-108">Return value</span></span>

<span data-ttu-id="3057f-109">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="3057f-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="3057f-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3057f-110">Return code</span></span>                                                                                           | <span data-ttu-id="3057f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3057f-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3057f-112"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="3057f-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="3057f-113">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="3057f-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="3057f-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="3057f-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="3057f-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3057f-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="3057f-116"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="3057f-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3057f-117">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="3057f-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3057f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3057f-118">Remarks</span></span>

<span data-ttu-id="3057f-119">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="3057f-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="3057f-120">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="3057f-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="3057f-121">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="3057f-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="3057f-122">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="3057f-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="3057f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3057f-123">Requirements</span></span>



| <span data-ttu-id="3057f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3057f-124">Requirement</span></span> | <span data-ttu-id="3057f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3057f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3057f-126">Header</span><span class="sxs-lookup"><span data-stu-id="3057f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3057f-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3057f-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3057f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3057f-128">Library</span></span><br/> | <dl> <span data-ttu-id="3057f-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3057f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3057f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3057f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3057f-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="3057f-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





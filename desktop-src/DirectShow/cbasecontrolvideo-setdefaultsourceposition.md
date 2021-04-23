---
description: Метод Сетдефаултсаурцепоситион задает для модуля подготовки отчетов использование расположения источника по умолчанию (обычно это все собственное видео).
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: Кбасеконтролвидео. Сетдефаултсаурцепоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6296683235a3cf051d0b9f4ee56ce51a3516f66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657109"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a><span data-ttu-id="09841-103">Кбасеконтролвидео. Сетдефаултсаурцепоситион, метод</span><span class="sxs-lookup"><span data-stu-id="09841-103">CBaseControlVideo.SetDefaultSourcePosition method</span></span>

<span data-ttu-id="09841-104">`SetDefaultSourcePosition`Метод задает для модуля подготовки отчетов использование исходной координаты по умолчанию (как правило, все собственное видео).</span><span class="sxs-lookup"><span data-stu-id="09841-104">The `SetDefaultSourcePosition` method sets the renderer back to using the default source position (typically all the native video).</span></span>

## <a name="syntax"></a><span data-ttu-id="09841-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09841-105">Syntax</span></span>


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a><span data-ttu-id="09841-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09841-106">Parameters</span></span>

<span data-ttu-id="09841-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="09841-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09841-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09841-108">Return value</span></span>

<span data-ttu-id="09841-109">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="09841-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="09841-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="09841-110">Return code</span></span>                                                                                           | <span data-ttu-id="09841-111">Описание</span><span class="sxs-lookup"><span data-stu-id="09841-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09841-112"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="09841-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="09841-113">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="09841-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="09841-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="09841-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="09841-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="09841-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="09841-116"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="09841-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="09841-117">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="09841-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09841-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09841-118">Remarks</span></span>

<span data-ttu-id="09841-119">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="09841-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="09841-120">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="09841-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="09841-121">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="09841-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="09841-122">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="09841-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="09841-123">Требования</span><span class="sxs-lookup"><span data-stu-id="09841-123">Requirements</span></span>



| <span data-ttu-id="09841-124">Требование</span><span class="sxs-lookup"><span data-stu-id="09841-124">Requirement</span></span> | <span data-ttu-id="09841-125">Значение</span><span class="sxs-lookup"><span data-stu-id="09841-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09841-126">Header</span><span class="sxs-lookup"><span data-stu-id="09841-126">Header</span></span><br/>  | <dl> <span data-ttu-id="09841-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09841-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09841-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09841-128">Library</span></span><br/> | <dl> <span data-ttu-id="09841-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="09841-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09841-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09841-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09841-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="09841-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





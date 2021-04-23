---
description: Метод Get \_ саурцелефт извлекает левую координату текущего исходного прямоугольника.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Метод CBaseControlVideo.get_SourceLeft (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657238"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="6e5fa-103">Кбасеконтролвидео. Get \_ саурцелефт, метод</span><span class="sxs-lookup"><span data-stu-id="6e5fa-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="6e5fa-104">`get_SourceLeft`Метод получает левую координату текущего прямоугольника источника.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e5fa-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="6e5fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e5fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5fa-107">*псаурцелефт*</span><span class="sxs-lookup"><span data-stu-id="6e5fa-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="6e5fa-108">Указатель на левую координату текущего исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5fa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e5fa-109">Return value</span></span>

<span data-ttu-id="6e5fa-110">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="6e5fa-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6e5fa-111">Return code</span></span>                                                                                           | <span data-ttu-id="6e5fa-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6e5fa-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e5fa-113"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="6e5fa-114">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6e5fa-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="6e5fa-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6e5fa-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6e5fa-118">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="6e5fa-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="6e5fa-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6e5fa-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e5fa-121">Remarks</span></span>

<span data-ttu-id="6e5fa-122">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="6e5fa-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="6e5fa-123">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="6e5fa-124">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="6e5fa-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="6e5fa-125">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="6e5fa-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5fa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6e5fa-126">Requirements</span></span>



| <span data-ttu-id="6e5fa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6e5fa-127">Requirement</span></span> | <span data-ttu-id="6e5fa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5fa-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5fa-129">Header</span><span class="sxs-lookup"><span data-stu-id="6e5fa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6e5fa-130"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e5fa-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6e5fa-131">Library</span></span><br/> | <dl> <span data-ttu-id="6e5fa-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6e5fa-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5fa-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e5fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5fa-134">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="6e5fa-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





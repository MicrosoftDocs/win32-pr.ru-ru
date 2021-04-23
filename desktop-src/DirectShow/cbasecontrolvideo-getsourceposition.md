---
description: Метод Жетсаурцепоситион извлекает расположение и размеры исходного прямоугольника в одной атомарной операции.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Кбасеконтролвидео. Жетсаурцепоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658128"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="7a823-103">Кбасеконтролвидео. Жетсаурцепоситион, метод</span><span class="sxs-lookup"><span data-stu-id="7a823-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="7a823-104">`GetSourcePosition`Метод получает расположение и размеры исходного прямоугольника в одной атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="7a823-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a823-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a823-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="7a823-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a823-107">*плефт*</span><span class="sxs-lookup"><span data-stu-id="7a823-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="7a823-108">Указатель на левую координату исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7a823-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7a823-109">*птоп*</span><span class="sxs-lookup"><span data-stu-id="7a823-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="7a823-110">Указатель на верхнюю координату исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7a823-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7a823-111">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="7a823-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="7a823-112">Указатель на ширину исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7a823-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7a823-113">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="7a823-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="7a823-114">Указатель на высоту исходного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7a823-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a823-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a823-115">Return value</span></span>

<span data-ttu-id="7a823-116">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="7a823-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="7a823-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7a823-117">Return code</span></span>                                                                                           | <span data-ttu-id="7a823-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7a823-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a823-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="7a823-120">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="7a823-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="7a823-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="7a823-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="7a823-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="7a823-123"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7a823-124">Невозможно выполнить операцию, так как ПИН-коды не подключены.</span><span class="sxs-lookup"><span data-stu-id="7a823-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="7a823-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="7a823-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7a823-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="7a823-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a823-127">Remarks</span></span>

<span data-ttu-id="7a823-128">Приложение может изменить исходный и конечный прямоугольники видео через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="7a823-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="7a823-129">Исходный прямоугольник влияет на то, какой раздел исходного видео будет отображаться на экране. прямоугольник назначения влияет на то, где будет отображаться видео при его воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="7a823-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="7a823-130">Прямоугольник назначения задается относительно клиентской области окна, в котором оно воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="7a823-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="7a823-131">Левый верхний угол окна имеет координаты (0, 0).</span><span class="sxs-lookup"><span data-stu-id="7a823-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a823-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7a823-132">Requirements</span></span>



| <span data-ttu-id="7a823-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7a823-133">Requirement</span></span> | <span data-ttu-id="7a823-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7a823-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a823-135">Header</span><span class="sxs-lookup"><span data-stu-id="7a823-135">Header</span></span><br/>  | <dl> <span data-ttu-id="7a823-136"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a823-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a823-137">Library</span></span><br/> | <dl> <span data-ttu-id="7a823-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7a823-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a823-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a823-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a823-140">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="7a823-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





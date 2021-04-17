---
description: Передает сообщение об \_ \_ изменении размера видео EC \_ в Диспетчер графов фильтров.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Кбасеконтролвидео. Онвидеосизечанже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665123"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="3d56a-103">Кбасеконтролвидео. Онвидеосизечанже, метод</span><span class="sxs-lookup"><span data-stu-id="3d56a-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="3d56a-104">Передает сообщение об \_ \_ изменении размера видео EC \_ в Диспетчер графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="3d56a-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d56a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d56a-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="3d56a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d56a-106">Parameters</span></span>

<span data-ttu-id="3d56a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3d56a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d56a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d56a-108">Return value</span></span>

<span data-ttu-id="3d56a-109">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="3d56a-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="3d56a-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3d56a-110">Return code</span></span>                                                                                   | <span data-ttu-id="3d56a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3d56a-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3d56a-112"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="3d56a-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3d56a-113">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="3d56a-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="3d56a-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3d56a-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3d56a-115">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3d56a-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d56a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d56a-116">Remarks</span></span>

<span data-ttu-id="3d56a-117">Модуль обработки видео должен вызывать эту функцию-член каждый раз при изменении размера видео; как правило, это вызывается один раз после первоначального соединения.</span><span class="sxs-lookup"><span data-stu-id="3d56a-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="3d56a-118">Если модуль подготовки отчетов поддерживает изменения в динамическом формате (от 320 x 240 до 160 x 120), он также должен вызываться после каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="3d56a-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d56a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3d56a-119">Requirements</span></span>



| <span data-ttu-id="3d56a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3d56a-120">Requirement</span></span> | <span data-ttu-id="3d56a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3d56a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d56a-122">Header</span><span class="sxs-lookup"><span data-stu-id="3d56a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3d56a-123"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d56a-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d56a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3d56a-124">Library</span></span><br/> | <dl> <span data-ttu-id="3d56a-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3d56a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d56a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d56a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d56a-127">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="3d56a-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





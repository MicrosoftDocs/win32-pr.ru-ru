---
description: Метод Get \_ фрамесдроппединрендерер Извлекает число кадров, отброшенных модулем подготовки отчетов.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Метод CBaseVideoRenderer.get_FramesDroppedInRenderer (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657102"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="a97dd-103">Кбасевидеорендерер. Get \_ фрамесдроппединрендерер, метод</span><span class="sxs-lookup"><span data-stu-id="a97dd-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="a97dd-104">`get_FramesDroppedInRenderer`Метод получает число кадров, отброшенных модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="a97dd-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a97dd-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="a97dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a97dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97dd-107">*пкфрамесдроппед*</span><span class="sxs-lookup"><span data-stu-id="a97dd-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="a97dd-108">Указатель на число отброшенных кадров.</span><span class="sxs-lookup"><span data-stu-id="a97dd-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97dd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a97dd-109">Return value</span></span>

<span data-ttu-id="a97dd-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a97dd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a97dd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a97dd-111">Remarks</span></span>

<span data-ttu-id="a97dd-112">Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдроппединрендерер**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) .</span><span class="sxs-lookup"><span data-stu-id="a97dd-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="a97dd-113">Таким способом страница свойств получает данные от планировщика.</span><span class="sxs-lookup"><span data-stu-id="a97dd-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="a97dd-114">Кадры также можно удалить из восходящего потока, не просматривая при этом модуль подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="a97dd-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97dd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a97dd-115">Requirements</span></span>



| <span data-ttu-id="a97dd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a97dd-116">Requirement</span></span> | <span data-ttu-id="a97dd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a97dd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a97dd-118">Header</span><span class="sxs-lookup"><span data-stu-id="a97dd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a97dd-119"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a97dd-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a97dd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a97dd-120">Library</span></span><br/> | <dl> <span data-ttu-id="a97dd-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a97dd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97dd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a97dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97dd-123">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="a97dd-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





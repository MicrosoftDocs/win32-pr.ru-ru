---
description: Метод EOS обновляет кэшированные метки времени после уведомления о завершении потока.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Крендерерпоспасссру. EOS, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658006"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="81a44-103">Крендерерпоспасссру. EOS, метод</span><span class="sxs-lookup"><span data-stu-id="81a44-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="81a44-104">`EOS`Метод обновляет кэшированные метки времени после уведомления о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="81a44-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81a44-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="81a44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81a44-106">Parameters</span></span>

<span data-ttu-id="81a44-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="81a44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81a44-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81a44-108">Return value</span></span>

<span data-ttu-id="81a44-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81a44-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="81a44-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="81a44-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="81a44-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81a44-111">Return code</span></span>                                                                            | <span data-ttu-id="81a44-112">Описание</span><span class="sxs-lookup"><span data-stu-id="81a44-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="81a44-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="81a44-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="81a44-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="81a44-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="81a44-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="81a44-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="81a44-116">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="81a44-116">Failure.</span></span> <span data-ttu-id="81a44-117">Возможно, фильтр не является потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="81a44-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81a44-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81a44-118">Remarks</span></span>

<span data-ttu-id="81a44-119">Этот метод должен вызываться фильтром при получении уведомления о завершении потока ([**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span><span class="sxs-lookup"><span data-stu-id="81a44-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="81a44-120">Метод устанавливает обе кэшированные отметки времени равными позиции окончания, гарантируя, что метод [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) возвращает правильные значения в конце потока.</span><span class="sxs-lookup"><span data-stu-id="81a44-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a44-121">Требования</span><span class="sxs-lookup"><span data-stu-id="81a44-121">Requirements</span></span>



| <span data-ttu-id="81a44-122">Требование</span><span class="sxs-lookup"><span data-stu-id="81a44-122">Requirement</span></span> | <span data-ttu-id="81a44-123">Значение</span><span class="sxs-lookup"><span data-stu-id="81a44-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a44-124">Header</span><span class="sxs-lookup"><span data-stu-id="81a44-124">Header</span></span><br/>  | <dl> <span data-ttu-id="81a44-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81a44-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81a44-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81a44-126">Library</span></span><br/> | <dl> <span data-ttu-id="81a44-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="81a44-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





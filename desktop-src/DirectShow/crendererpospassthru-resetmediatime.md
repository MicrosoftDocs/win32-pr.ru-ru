---
description: Метод Ресетмедиатиме Сбрасывает кэшированные отметки времени в ноль.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Крендерерпоспасссру. Ресетмедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657172"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="8a5b3-103">Крендерерпоспасссру. Ресетмедиатиме, метод</span><span class="sxs-lookup"><span data-stu-id="8a5b3-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="8a5b3-104">`ResetMediaTime`Метод сбрасывает кэшированные отметки времени в ноль.</span><span class="sxs-lookup"><span data-stu-id="8a5b3-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a5b3-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="8a5b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a5b3-106">Parameters</span></span>

<span data-ttu-id="8a5b3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8a5b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a5b3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a5b3-108">Return value</span></span>

<span data-ttu-id="8a5b3-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8a5b3-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5b3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a5b3-110">Remarks</span></span>

<span data-ttu-id="8a5b3-111">Фильтр должен вызывать этот метод всякий раз, когда отметки времени, кэшированные методом [**крендерерпоспасссру:: регистермедиатиме**](crendererpospassthru-registermediatime.md) , становятся недействительными.</span><span class="sxs-lookup"><span data-stu-id="8a5b3-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="8a5b3-112">В частности, он должен вызывать этот метод в ответ на методы [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) и [**Имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="8a5b3-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="8a5b3-113">После вызова этого метода метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) возвращает ноль для времени начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="8a5b3-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5b3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8a5b3-114">Requirements</span></span>



| <span data-ttu-id="8a5b3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8a5b3-115">Requirement</span></span> | <span data-ttu-id="8a5b3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8a5b3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5b3-117">Header</span><span class="sxs-lookup"><span data-stu-id="8a5b3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8a5b3-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a5b3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a5b3-119">Library</span></span><br/> | <dl> <span data-ttu-id="8a5b3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





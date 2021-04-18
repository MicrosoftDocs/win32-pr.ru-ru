---
description: Метод размещения \_ StopTime задает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиапоситион::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Метод CPosPassThru.put_StopTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658013"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="c583a-104">Кпоспасссру. размещение \_ метода StopTime</span><span class="sxs-lookup"><span data-stu-id="c583a-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="c583a-105">`put_StopTime`Метод задает время, когда воспроизведение будет останавливаться, относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="c583a-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="c583a-106">Этот метод реализует метод [**имедиапоситион::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="c583a-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c583a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c583a-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="c583a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c583a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c583a-109">*ллтиме*</span><span class="sxs-lookup"><span data-stu-id="c583a-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c583a-110">Время окончания в секундах. </span><span class="sxs-lookup"><span data-stu-id="c583a-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c583a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c583a-111">Return value</span></span>

<span data-ttu-id="c583a-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c583a-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c583a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c583a-113">Requirements</span></span>



| <span data-ttu-id="c583a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c583a-114">Requirement</span></span> | <span data-ttu-id="c583a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c583a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c583a-116">Header</span><span class="sxs-lookup"><span data-stu-id="c583a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c583a-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c583a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c583a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c583a-118">Library</span></span><br/> | <dl> <span data-ttu-id="c583a-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c583a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c583a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c583a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c583a-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="c583a-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





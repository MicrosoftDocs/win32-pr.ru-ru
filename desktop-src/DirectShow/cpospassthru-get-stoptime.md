---
description: 'Метод Get \_ StopTime извлекает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиапоситион:: Get \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Метод CPosPassThru.get_StopTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657230"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="e4213-104">Кпоспасссру. Get \_ StopTime, метод</span><span class="sxs-lookup"><span data-stu-id="e4213-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="e4213-105">`get_StopTime`Метод получает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="e4213-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="e4213-106">Этот метод реализует метод [**имедиапоситион:: Get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="e4213-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4213-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4213-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="e4213-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4213-109">*пллтиме*</span><span class="sxs-lookup"><span data-stu-id="e4213-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e4213-110">Указатель на переменную, которая получает время окончания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="e4213-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4213-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4213-111">Return value</span></span>

<span data-ttu-id="e4213-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e4213-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4213-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e4213-113">Requirements</span></span>



| <span data-ttu-id="e4213-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e4213-114">Requirement</span></span> | <span data-ttu-id="e4213-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e4213-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4213-116">Header</span><span class="sxs-lookup"><span data-stu-id="e4213-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4213-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4213-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4213-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4213-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4213-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e4213-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4213-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4213-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4213-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e4213-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





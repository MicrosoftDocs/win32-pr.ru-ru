---
description: 'Метод Жетстоппоситион извлекает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиасикинг:: Жетстоппоситион.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Кпоспасссру. Жетстоппоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679967"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="e0388-104">Кпоспасссру. Жетстоппоситион, метод</span><span class="sxs-lookup"><span data-stu-id="e0388-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="e0388-105">`GetStopPosition`Метод получает время, когда воспроизведение будет прервано относительно длительности потока.</span><span class="sxs-lookup"><span data-stu-id="e0388-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="e0388-106">Этот метод реализует метод [**имедиасикинг:: жетстоппоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="e0388-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0388-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0388-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="e0388-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0388-109">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="e0388-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="e0388-110">Указатель на переменную, которая получает время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="e0388-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0388-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0388-111">Return value</span></span>

<span data-ttu-id="e0388-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="e0388-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0388-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e0388-113">Requirements</span></span>



| <span data-ttu-id="e0388-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e0388-114">Requirement</span></span> | <span data-ttu-id="e0388-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e0388-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0388-116">Header</span><span class="sxs-lookup"><span data-stu-id="e0388-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0388-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0388-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0388-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0388-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0388-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0388-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0388-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0388-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0388-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e0388-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





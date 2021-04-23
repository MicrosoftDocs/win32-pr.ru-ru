---
description: 'Метод Rate извлекает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Rate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Метод Кпоспасссру. rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657003"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="4be5b-104">Кпоспасссру. метод Rate</span><span class="sxs-lookup"><span data-stu-id="4be5b-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="4be5b-105">`GetRate`Метод получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4be5b-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="4be5b-106">Этот метод реализует метод [**имедиасикинг:: Rate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="4be5b-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4be5b-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="4be5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4be5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be5b-109">*пдрате*</span><span class="sxs-lookup"><span data-stu-id="4be5b-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="4be5b-110">Указатель на переменную, которая получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4be5b-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be5b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4be5b-111">Return value</span></span>

<span data-ttu-id="4be5b-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4be5b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be5b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4be5b-113">Requirements</span></span>



| <span data-ttu-id="4be5b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4be5b-114">Requirement</span></span> | <span data-ttu-id="4be5b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4be5b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be5b-116">Header</span><span class="sxs-lookup"><span data-stu-id="4be5b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4be5b-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4be5b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4be5b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4be5b-118">Library</span></span><br/> | <dl> <span data-ttu-id="4be5b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4be5b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be5b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4be5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be5b-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="4be5b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





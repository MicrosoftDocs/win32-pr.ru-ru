---
description: 'Кпоспасссру. метод Rate — метод метода Rate извлекает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Rate.'
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
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085562"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="d8599-104">Кпоспасссру. метод Rate</span><span class="sxs-lookup"><span data-stu-id="d8599-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="d8599-105">`GetRate`Метод получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8599-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="d8599-106">Этот метод реализует метод [**имедиасикинг:: Rate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="d8599-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8599-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8599-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="d8599-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8599-109">*пдрате*</span><span class="sxs-lookup"><span data-stu-id="d8599-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d8599-110">Указатель на переменную, которая получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8599-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8599-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8599-111">Return value</span></span>

<span data-ttu-id="d8599-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d8599-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8599-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d8599-113">Requirements</span></span>



| <span data-ttu-id="d8599-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d8599-114">Requirement</span></span> | <span data-ttu-id="d8599-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d8599-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8599-116">Header</span><span class="sxs-lookup"><span data-stu-id="d8599-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d8599-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8599-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8599-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8599-118">Library</span></span><br/> | <dl> <span data-ttu-id="d8599-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d8599-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8599-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d8599-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8599-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="d8599-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





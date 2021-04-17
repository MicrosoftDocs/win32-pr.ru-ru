---
description: 'Метод получения \_ длительности извлекает длительность потока. Этот метод реализует метод Имедиапоситион:: Get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Метод CPosPassThru.get_Duration (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679845"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="cdc2e-104">Кпоспасссру. Get \_ Duration, метод</span><span class="sxs-lookup"><span data-stu-id="cdc2e-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="cdc2e-105">`get_Duration`Метод получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="cdc2e-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="cdc2e-106">Этот метод реализует метод [**имедиапоситион:: Get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="cdc2e-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc2e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdc2e-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="cdc2e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdc2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc2e-109">*пленгс*</span><span class="sxs-lookup"><span data-stu-id="cdc2e-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc2e-110">Указатель на переменную, которая получает общую длину потока в секундах.</span><span class="sxs-lookup"><span data-stu-id="cdc2e-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc2e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdc2e-111">Return value</span></span>

<span data-ttu-id="cdc2e-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cdc2e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc2e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cdc2e-113">Requirements</span></span>



| <span data-ttu-id="cdc2e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cdc2e-114">Requirement</span></span> | <span data-ttu-id="cdc2e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cdc2e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc2e-116">Header</span><span class="sxs-lookup"><span data-stu-id="cdc2e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cdc2e-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc2e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdc2e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cdc2e-118">Library</span></span><br/> | <dl> <span data-ttu-id="cdc2e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc2e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc2e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdc2e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc2e-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="cdc2e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





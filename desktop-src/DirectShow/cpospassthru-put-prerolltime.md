---
description: Метод размещения \_ прероллтиме задает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиапоситион::p UT \_ прероллтиме.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Метод CPosPassThru.put_PrerollTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657537"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="d03e7-104">Кпоспасссру. размещение \_ метода прероллтиме</span><span class="sxs-lookup"><span data-stu-id="d03e7-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="d03e7-105">`put_PrerollTime`Метод задает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="d03e7-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="d03e7-106">Этот метод реализует метод [**имедиапоситион::p UT \_ прероллтиме**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="d03e7-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d03e7-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="d03e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d03e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d03e7-109">*ллтиме*</span><span class="sxs-lookup"><span data-stu-id="d03e7-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d03e7-110">Время в секундах.</span><span class="sxs-lookup"><span data-stu-id="d03e7-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d03e7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d03e7-111">Return value</span></span>

<span data-ttu-id="d03e7-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d03e7-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d03e7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d03e7-113">Requirements</span></span>



| <span data-ttu-id="d03e7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d03e7-114">Requirement</span></span> | <span data-ttu-id="d03e7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d03e7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d03e7-116">Header</span><span class="sxs-lookup"><span data-stu-id="d03e7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d03e7-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d03e7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d03e7-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d03e7-118">Library</span></span><br/> | <dl> <span data-ttu-id="d03e7-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d03e7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03e7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d03e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03e7-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="d03e7-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





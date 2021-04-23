---
description: 'Метод Get \_ прероллтиме извлекает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиапоситион:: Get \_ прероллтиме.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Метод CPosPassThru.get_PrerollTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657273"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="bbc5b-104">Кпоспасссру. Get \_ прероллтиме, метод</span><span class="sxs-lookup"><span data-stu-id="bbc5b-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="bbc5b-105">`get_PrerollTime`Метод получает объем данных, которые будут помещены в очередь перед начальной позицией.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="bbc5b-106">Этот метод реализует метод [**имедиапоситион:: Get \_ прероллтиме**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="bbc5b-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbc5b-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="bbc5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbc5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc5b-109">*пллтиме*</span><span class="sxs-lookup"><span data-stu-id="bbc5b-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bbc5b-110">Указатель на переменную, которая получает время в секундах.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc5b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbc5b-111">Return value</span></span>

<span data-ttu-id="bbc5b-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="bbc5b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc5b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bbc5b-113">Requirements</span></span>



| <span data-ttu-id="bbc5b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc5b-114">Requirement</span></span> | <span data-ttu-id="bbc5b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc5b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5b-116">Header</span><span class="sxs-lookup"><span data-stu-id="bbc5b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bbc5b-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbc5b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bbc5b-118">Library</span></span><br/> | <dl> <span data-ttu-id="bbc5b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc5b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbc5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc5b-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="bbc5b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





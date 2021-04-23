---
description: 'Метод получения \_ скорости получает скорость воспроизведения. Этот метод реализует метод Имедиапоситион:: Get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Метод CPosPassThru.get_Rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675453"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="7c34a-104">Кпоспасссру. получение \_ метода Rate</span><span class="sxs-lookup"><span data-stu-id="7c34a-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="7c34a-105">`get_Rate`Метод получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7c34a-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="7c34a-106">Этот метод реализует метод [**имедиапоситион:: Get \_**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .</span><span class="sxs-lookup"><span data-stu-id="7c34a-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c34a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c34a-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="7c34a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c34a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c34a-109">*пдрате*</span><span class="sxs-lookup"><span data-stu-id="7c34a-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="7c34a-110">Указатель на переменную, которая получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7c34a-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c34a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c34a-111">Return value</span></span>

<span data-ttu-id="7c34a-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="7c34a-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c34a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7c34a-113">Requirements</span></span>



| <span data-ttu-id="7c34a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7c34a-114">Requirement</span></span> | <span data-ttu-id="7c34a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7c34a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c34a-116">Header</span><span class="sxs-lookup"><span data-stu-id="7c34a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7c34a-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c34a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c34a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c34a-118">Library</span></span><br/> | <dl> <span data-ttu-id="7c34a-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7c34a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c34a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c34a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c34a-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="7c34a-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





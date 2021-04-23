---
description: Метод WebMethod извлекает идентификатор класса фильтра. Этот метод реализует метод IPersist::/ClassID.
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Метод Кбасефилтер. ClassID (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657436"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="4da50-104">Кбасефилтер. ClassID, метод</span><span class="sxs-lookup"><span data-stu-id="4da50-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="4da50-105">`GetClassID`Метод получает идентификатор класса фильтра.</span><span class="sxs-lookup"><span data-stu-id="4da50-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="4da50-106">Этот метод реализует метод **IPersist::/ClassID** .</span><span class="sxs-lookup"><span data-stu-id="4da50-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da50-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4da50-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="4da50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4da50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da50-109">*пклсид*</span><span class="sxs-lookup"><span data-stu-id="4da50-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="4da50-110">Указатель на переменную, которая получает идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="4da50-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da50-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4da50-111">Return value</span></span>

<span data-ttu-id="4da50-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="4da50-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da50-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4da50-113">Requirements</span></span>



| <span data-ttu-id="4da50-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4da50-114">Requirement</span></span> | <span data-ttu-id="4da50-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4da50-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da50-116">Header</span><span class="sxs-lookup"><span data-stu-id="4da50-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4da50-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4da50-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4da50-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4da50-118">Library</span></span><br/> | <dl> <span data-ttu-id="4da50-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4da50-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da50-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4da50-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da50-121">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="4da50-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





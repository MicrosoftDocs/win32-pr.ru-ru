---
description: Метод конструктора Ксистемклокк. Ксистемклокк.
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Конструктор Ксистемклокк. Ксистемклокк (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095202"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="3bcfc-103">Ксистемклокк. Ксистемклокк, конструктор</span><span class="sxs-lookup"><span data-stu-id="3bcfc-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="3bcfc-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcfc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bcfc-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="3bcfc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bcfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bcfc-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3bcfc-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3bcfc-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-108">String containing the debug name of the object.</span></span> <span data-ttu-id="3bcfc-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3bcfc-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcfc-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3bcfc-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3bcfc-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3bcfc-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3bcfc-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3bcfc-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="3bcfc-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3bcfc-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3bcfc-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="3bcfc-116">При возникновении ошибки метод возвращает код ошибки в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="3bcfc-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bcfc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3bcfc-117">Requirements</span></span>



| <span data-ttu-id="3bcfc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3bcfc-118">Requirement</span></span> | <span data-ttu-id="3bcfc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3bcfc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcfc-120">Header</span><span class="sxs-lookup"><span data-stu-id="3bcfc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3bcfc-121"><dt>Сисклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bcfc-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3bcfc-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3bcfc-122">Library</span></span><br/> | <dl> <span data-ttu-id="3bcfc-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3bcfc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





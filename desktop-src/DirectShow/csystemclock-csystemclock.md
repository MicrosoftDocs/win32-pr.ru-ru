---
description: Метод конструктора.
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
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657661"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="1137e-103">Ксистемклокк. Ксистемклокк, конструктор</span><span class="sxs-lookup"><span data-stu-id="1137e-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="1137e-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="1137e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1137e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1137e-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1137e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1137e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1137e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1137e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1137e-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="1137e-108">String containing the debug name of the object.</span></span> <span data-ttu-id="1137e-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1137e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1137e-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="1137e-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1137e-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="1137e-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="1137e-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="1137e-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="1137e-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1137e-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1137e-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="1137e-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1137e-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1137e-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="1137e-116">При возникновении ошибки метод возвращает код ошибки в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="1137e-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1137e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1137e-117">Requirements</span></span>



| <span data-ttu-id="1137e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1137e-118">Requirement</span></span> | <span data-ttu-id="1137e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1137e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1137e-120">Header</span><span class="sxs-lookup"><span data-stu-id="1137e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1137e-121"><dt>Сисклокк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1137e-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1137e-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1137e-122">Library</span></span><br/> | <dl> <span data-ttu-id="1137e-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1137e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





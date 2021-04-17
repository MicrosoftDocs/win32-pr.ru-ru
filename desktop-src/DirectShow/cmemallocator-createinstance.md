---
description: Метод CreateInstance создает новый экземпляр класса Кмемаллокатор.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Метод Кмемаллокатор. CreateInstance (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665496"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="a57b5-103">Кмемаллокатор. CreateInstance, метод</span><span class="sxs-lookup"><span data-stu-id="a57b5-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="a57b5-104">`CreateInstance`Метод создает новый экземпляр класса **кмемаллокатор** .</span><span class="sxs-lookup"><span data-stu-id="a57b5-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a57b5-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="a57b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a57b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a57b5-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a57b5-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a57b5-108">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="a57b5-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="a57b5-109">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="a57b5-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a57b5-110">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a57b5-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a57b5-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="a57b5-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a57b5-112">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="a57b5-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a57b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a57b5-113">Return value</span></span>

<span data-ttu-id="a57b5-114">Возвращает указатель на новый объект **кмемаллокатор** , типизированный как объект **кункновн** .</span><span class="sxs-lookup"><span data-stu-id="a57b5-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57b5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a57b5-115">Requirements</span></span>



| <span data-ttu-id="a57b5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a57b5-116">Requirement</span></span> | <span data-ttu-id="a57b5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a57b5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57b5-118">Header</span><span class="sxs-lookup"><span data-stu-id="a57b5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a57b5-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a57b5-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a57b5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a57b5-120">Library</span></span><br/> | <dl> <span data-ttu-id="a57b5-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a57b5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57b5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a57b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57b5-123">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="a57b5-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





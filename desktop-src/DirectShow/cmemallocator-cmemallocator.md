---
description: Метод конструктора Кмемаллокатор. Кмемаллокатор.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Конструктор Кмемаллокатор. Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095402"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="c4658-103">Кмемаллокатор. Кмемаллокатор, конструктор</span><span class="sxs-lookup"><span data-stu-id="c4658-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="c4658-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c4658-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4658-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4658-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c4658-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4658-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4658-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c4658-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c4658-108">Указатель на строку, содержащую имя распределителя.</span><span class="sxs-lookup"><span data-stu-id="c4658-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="c4658-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="c4658-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c4658-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="c4658-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="c4658-111">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="c4658-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c4658-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c4658-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4658-113">*фр*</span><span class="sxs-lookup"><span data-stu-id="c4658-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c4658-114">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="c4658-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4658-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c4658-115">Requirements</span></span>



| <span data-ttu-id="c4658-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c4658-116">Requirement</span></span> | <span data-ttu-id="c4658-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c4658-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4658-118">Header</span><span class="sxs-lookup"><span data-stu-id="c4658-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c4658-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4658-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4658-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4658-120">Library</span></span><br/> | <dl> <span data-ttu-id="c4658-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c4658-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4658-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c4658-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4658-123">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="c4658-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





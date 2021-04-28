---
description: Метод конструктора Кмедиасампле. Кмедиасампле.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Конструктор Кмедиасампле. Кмедиасампле (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095442"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="5d2f9-103">Кмедиасампле. Кмедиасампле, конструктор</span><span class="sxs-lookup"><span data-stu-id="5d2f9-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="5d2f9-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d2f9-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="5d2f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d2f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2f9-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="5d2f9-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f9-108">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f9-109">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="5d2f9-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f9-110">Указатель на объект [**кбасеаллокатор**](cbaseallocator.md) , который создал этот образец.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f9-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="5d2f9-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f9-112">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f9-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="5d2f9-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f9-114">Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f9-115">*length*</span><span class="sxs-lookup"><span data-stu-id="5d2f9-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="5d2f9-116">Длина буфера памяти.</span><span class="sxs-lookup"><span data-stu-id="5d2f9-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d2f9-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d2f9-117">Remarks</span></span>

<span data-ttu-id="5d2f9-118">Базовый класс не изменяет значение **HRESULT** , передаваемое в параметре *фр* .</span><span class="sxs-lookup"><span data-stu-id="5d2f9-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2f9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5d2f9-119">Requirements</span></span>



| <span data-ttu-id="5d2f9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5d2f9-120">Requirement</span></span> | <span data-ttu-id="5d2f9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5d2f9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2f9-122">Header</span><span class="sxs-lookup"><span data-stu-id="5d2f9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5d2f9-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f9-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5d2f9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d2f9-124">Library</span></span><br/> | <dl> <span data-ttu-id="5d2f9-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2f9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5d2f9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2f9-127">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="5d2f9-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





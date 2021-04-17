---
description: Метод конструктора.
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
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675203"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="f61eb-103">Кмедиасампле. Кмедиасампле, конструктор</span><span class="sxs-lookup"><span data-stu-id="f61eb-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="f61eb-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f61eb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f61eb-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="f61eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f61eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61eb-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f61eb-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f61eb-108">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="f61eb-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f61eb-109">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="f61eb-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="f61eb-110">Указатель на объект [**кбасеаллокатор**](cbaseallocator.md) , который создал этот образец.</span><span class="sxs-lookup"><span data-stu-id="f61eb-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="f61eb-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="f61eb-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f61eb-112">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="f61eb-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f61eb-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="f61eb-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f61eb-114">Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера.</span><span class="sxs-lookup"><span data-stu-id="f61eb-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="f61eb-115">*length*</span><span class="sxs-lookup"><span data-stu-id="f61eb-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="f61eb-116">Длина буфера памяти.</span><span class="sxs-lookup"><span data-stu-id="f61eb-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f61eb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f61eb-117">Remarks</span></span>

<span data-ttu-id="f61eb-118">Базовый класс не изменяет значение **HRESULT** , передаваемое в параметре *фр* .</span><span class="sxs-lookup"><span data-stu-id="f61eb-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61eb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f61eb-119">Requirements</span></span>



| <span data-ttu-id="f61eb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f61eb-120">Requirement</span></span> | <span data-ttu-id="f61eb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f61eb-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61eb-122">Header</span><span class="sxs-lookup"><span data-stu-id="f61eb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f61eb-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f61eb-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f61eb-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f61eb-124">Library</span></span><br/> | <dl> <span data-ttu-id="f61eb-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f61eb-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61eb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f61eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61eb-127">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="f61eb-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





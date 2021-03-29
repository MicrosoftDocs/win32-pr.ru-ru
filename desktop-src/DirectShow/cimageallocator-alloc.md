---
description: 'Метод Alloc выделяет память для буферов. Этот метод переопределяет метод Кбасеаллокатор:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Метод Цимажеаллокатор. Alloc (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657544"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="6431a-104">Цимажеаллокатор. Alloc, метод</span><span class="sxs-lookup"><span data-stu-id="6431a-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="6431a-105">`Alloc`Метод выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="6431a-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="6431a-106">Этот метод переопределяет метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="6431a-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6431a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6431a-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="6431a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6431a-108">Parameters</span></span>

<span data-ttu-id="6431a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6431a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6431a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6431a-110">Return value</span></span>

<span data-ttu-id="6431a-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6431a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6431a-112">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="6431a-112">Possible values include the following.</span></span>



| <span data-ttu-id="6431a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6431a-113">Return code</span></span>                                                                                   | <span data-ttu-id="6431a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6431a-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="6431a-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6431a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6431a-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="6431a-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="6431a-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6431a-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6431a-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="6431a-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6431a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6431a-119">Remarks</span></span>

<span data-ttu-id="6431a-120">Этот метод вызывается методом [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) , когда фильтр фиксирует распределитель.</span><span class="sxs-lookup"><span data-stu-id="6431a-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="6431a-121">Этот метод создает список образцов мультимедиа, которые реализуются как объекты [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="6431a-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="6431a-122">Каждый пример содержит аппаратно-независимый точечный рисунок GDI с помощью функции GDI **креатедибсектион** .</span><span class="sxs-lookup"><span data-stu-id="6431a-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="6431a-123">Внутренний метод вызывает [**Цимажеаллокатор:: креатедиб**](cimageallocator-createdib.md) для создания каждого DIB, а [**Цимажеаллокатор:: креатеимажесампле**](cimageallocator-createimagesample.md) — для создания каждого образца.</span><span class="sxs-lookup"><span data-stu-id="6431a-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="6431a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6431a-124">Requirements</span></span>



| <span data-ttu-id="6431a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6431a-125">Requirement</span></span> | <span data-ttu-id="6431a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6431a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6431a-127">Header</span><span class="sxs-lookup"><span data-stu-id="6431a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6431a-128"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6431a-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6431a-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6431a-129">Library</span></span><br/> | <dl> <span data-ttu-id="6431a-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6431a-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6431a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6431a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6431a-132">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="6431a-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 





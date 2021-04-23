---
description: Метод Alloc выделяет память для буферов.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Метод Кбасеаллокатор. Alloc (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665068"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="0f5ab-103">Кбасеаллокатор. Alloc, метод</span><span class="sxs-lookup"><span data-stu-id="0f5ab-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="0f5ab-104">`Alloc`Метод выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f5ab-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="0f5ab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f5ab-106">Parameters</span></span>

<span data-ttu-id="0f5ab-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f5ab-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f5ab-108">Return value</span></span>

<span data-ttu-id="0f5ab-109">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f5ab-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="0f5ab-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0f5ab-110">Return code</span></span>                                                                                       | <span data-ttu-id="0f5ab-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0f5ab-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0f5ab-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="0f5ab-113">Требования к буферу не изменились.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="0f5ab-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="0f5ab-115">Требования к буферу изменились.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="0f5ab-116"><dt>**VFW \_ E \_ сизенотсет**</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="0f5ab-117">Не заданы требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0f5ab-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f5ab-118">Remarks</span></span>

<span data-ttu-id="0f5ab-119">Этот метод вызывается методом [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="0f5ab-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="0f5ab-120">В базовом классе этот метод не выделяет память.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="0f5ab-121">Он возвращает ошибку, если требования к буферу не были заданы, S \_ false, если требования не изменялись, и \_ ОК, если требования были изменены.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="0f5ab-122">Производный класс должен переопределять этот метод для выполнения фактического выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="0f5ab-123">Как правило, производный класс выполнит следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="0f5ab-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="0f5ab-124">Вызовите реализацию базового класса, чтобы определить, требуется ли выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="0f5ab-125">Выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-125">Allocate memory.</span></span>
3.  <span data-ttu-id="0f5ab-126">Создание объектов [**кмедиасампле**](cmediasample.md) , содержащих блоки памяти, из шага 2.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="0f5ab-127">Добавьте каждый объект **кмедиасампле** в список бесплатных примеров ([**кбасеаллокатор:: m \_ лфри**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="0f5ab-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="0f5ab-128">Пример см. в разделе [**кмемаллокатор:: Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="0f5ab-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5ab-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0f5ab-129">Requirements</span></span>



| <span data-ttu-id="0f5ab-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0f5ab-130">Requirement</span></span> | <span data-ttu-id="0f5ab-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0f5ab-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ab-132">Header</span><span class="sxs-lookup"><span data-stu-id="0f5ab-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0f5ab-133"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f5ab-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f5ab-134">Library</span></span><br/> | <dl> <span data-ttu-id="0f5ab-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f5ab-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f5ab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ab-137">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="0f5ab-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





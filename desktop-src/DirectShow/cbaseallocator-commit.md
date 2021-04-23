---
description: 'Метод Commit выделяет память для буферов. Этот метод реализует метод Имемаллокатор:: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Метод Кбасеаллокатор. Commit (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668550"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="a3038-104">Кбасеаллокатор. Commit, метод</span><span class="sxs-lookup"><span data-stu-id="a3038-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="a3038-105">`Commit`Метод выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="a3038-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="a3038-106">Этот метод реализует метод [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .</span><span class="sxs-lookup"><span data-stu-id="a3038-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3038-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3038-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="a3038-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3038-108">Parameters</span></span>

<span data-ttu-id="a3038-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a3038-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3038-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3038-110">Return value</span></span>

<span data-ttu-id="a3038-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3038-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a3038-112">Возможные значения перечислены в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="a3038-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="a3038-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a3038-113">Return code</span></span>                                                                                       | <span data-ttu-id="a3038-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a3038-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="a3038-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a3038-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a3038-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a3038-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="a3038-117"><dt>**VFW \_ E \_ сизенотсет**</dt></span><span class="sxs-lookup"><span data-stu-id="a3038-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="a3038-118">Не указаны требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="a3038-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3038-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3038-119">Remarks</span></span>

<span data-ttu-id="a3038-120">Перед вызовом этого метода вызовите метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) , чтобы указать требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="a3038-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="a3038-121">Этот метод вызывает виртуальный метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) , чтобы выделить память для буферов.</span><span class="sxs-lookup"><span data-stu-id="a3038-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="a3038-122">Производные классы могут переопределять **Alloc**.</span><span class="sxs-lookup"><span data-stu-id="a3038-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="a3038-123">Если операция отмены фиксации отложена, она отменяется.</span><span class="sxs-lookup"><span data-stu-id="a3038-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="a3038-124">Этот метод необходимо вызвать перед вызовом метода [**кбасеаллокатор:: with buffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a3038-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3038-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a3038-125">Requirements</span></span>



| <span data-ttu-id="a3038-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a3038-126">Requirement</span></span> | <span data-ttu-id="a3038-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a3038-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3038-128">Header</span><span class="sxs-lookup"><span data-stu-id="a3038-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a3038-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3038-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3038-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3038-130">Library</span></span><br/> | <dl> <span data-ttu-id="a3038-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a3038-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3038-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3038-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3038-133">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="a3038-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





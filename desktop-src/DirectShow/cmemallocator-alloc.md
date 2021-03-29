---
description: Метод Alloc выделяет память для буферов.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Метод Кмемаллокатор. Alloc (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665498"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="d03e6-103">Кмемаллокатор. Alloc, метод</span><span class="sxs-lookup"><span data-stu-id="d03e6-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="d03e6-104">`Alloc`Метод выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="d03e6-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d03e6-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="d03e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d03e6-106">Parameters</span></span>

<span data-ttu-id="d03e6-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d03e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d03e6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d03e6-108">Return value</span></span>

<span data-ttu-id="d03e6-109">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d03e6-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d03e6-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d03e6-110">Return code</span></span>                                                                                       | <span data-ttu-id="d03e6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d03e6-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d03e6-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d03e6-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="d03e6-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d03e6-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="d03e6-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d03e6-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="d03e6-115">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="d03e6-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="d03e6-116"><dt>**VFW \_ E \_ сизенотсет**</dt></span><span class="sxs-lookup"><span data-stu-id="d03e6-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="d03e6-117">Не заданы требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="d03e6-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d03e6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d03e6-118">Remarks</span></span>

<span data-ttu-id="d03e6-119">Этот метод вызывается методом [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="d03e6-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="d03e6-120">Он выделяет непрерывный блок памяти, достаточный для требований к буферу, заданным в методе [**кмемаллокатор:: SetProperties**](cmemallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="d03e6-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d03e6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d03e6-121">Requirements</span></span>



| <span data-ttu-id="d03e6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d03e6-122">Requirement</span></span> | <span data-ttu-id="d03e6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d03e6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d03e6-124">Header</span><span class="sxs-lookup"><span data-stu-id="d03e6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d03e6-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d03e6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d03e6-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d03e6-126">Library</span></span><br/> | <dl> <span data-ttu-id="d03e6-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d03e6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03e6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d03e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03e6-129">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="d03e6-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





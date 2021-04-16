---
description: Указатель на блок памяти, содержащий буферы.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Элемент Кмемаллокатор:: m_pBuffer (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680045"
---
# <a name="cmemallocatorm_pbuffer-member"></a><span data-ttu-id="f542d-103">Элемент Кмемаллокатор:: m \_ pBuffer</span><span class="sxs-lookup"><span data-stu-id="f542d-103">CMemAllocator::m\_pBuffer member</span></span>

<span data-ttu-id="f542d-104">Указатель на блок памяти, содержащий буферы.</span><span class="sxs-lookup"><span data-stu-id="f542d-104">Pointer to the memory block that contains the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f542d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f542d-105">Syntax</span></span>


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a><span data-ttu-id="f542d-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="f542d-106">Remarks</span></span>

<span data-ttu-id="f542d-107">Буферы выборки вычисляются как смещения от этого указателя.</span><span class="sxs-lookup"><span data-stu-id="f542d-107">Sample buffers are calculated as offsets from this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f542d-108">Требования</span><span class="sxs-lookup"><span data-stu-id="f542d-108">Requirements</span></span>



| <span data-ttu-id="f542d-109">Требование</span><span class="sxs-lookup"><span data-stu-id="f542d-109">Requirement</span></span> | <span data-ttu-id="f542d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f542d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f542d-111">Header</span><span class="sxs-lookup"><span data-stu-id="f542d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f542d-112"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f542d-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f542d-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f542d-113">Library</span></span><br/> | <dl> <span data-ttu-id="f542d-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f542d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f542d-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f542d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f542d-116">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="f542d-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





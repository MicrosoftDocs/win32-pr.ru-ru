---
description: Указатель на распределитель, создавший этот образец.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Элемент Кмедиасампле:: m_pAllocator (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665203"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="dbc5b-103">Элемент Кмедиасампле:: m \_ паллокатор</span><span class="sxs-lookup"><span data-stu-id="dbc5b-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="dbc5b-104">Указатель на распределитель, создавший этот образец.</span><span class="sxs-lookup"><span data-stu-id="dbc5b-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc5b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc5b-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="dbc5b-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbc5b-106">Remarks</span></span>

<span data-ttu-id="dbc5b-107">Несмотря на то, что образец хранит указатель на распределитель, он не содержит счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="dbc5b-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="dbc5b-108">Вместо этого распределитель увеличивает свой счетчик ссылок в методе [**имемаллокатор::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) IsReference и освобождает себя в методе [**Имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="dbc5b-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="dbc5b-109">Это гарантирует, что распределитель будет доступен, пока другой объект использует этот пример.</span><span class="sxs-lookup"><span data-stu-id="dbc5b-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc5b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="dbc5b-110">Requirements</span></span>



| <span data-ttu-id="dbc5b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="dbc5b-111">Requirement</span></span> | <span data-ttu-id="dbc5b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc5b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc5b-113">Header</span><span class="sxs-lookup"><span data-stu-id="dbc5b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc5b-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc5b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbc5b-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbc5b-115">Library</span></span><br/> | <dl> <span data-ttu-id="dbc5b-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc5b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc5b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbc5b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc5b-118">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="dbc5b-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





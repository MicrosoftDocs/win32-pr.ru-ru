---
description: Метод Нотифяллокатор информирует объект Кдравимаже о том, является ли распределитель для соединения объектом Цимажеаллокатор.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Кдравимаже. Нотифяллокатор, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679763"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="90aed-103">Кдравимаже. Нотифяллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="90aed-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="90aed-104">`NotifyAllocator`Метод информирует объект **кдравимаже** о том, является ли распределитель для соединения объектом [**Цимажеаллокатор**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="90aed-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="90aed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90aed-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="90aed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90aed-107">*бусингимажеаллокатор*</span><span class="sxs-lookup"><span data-stu-id="90aed-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="90aed-108">Логическое значение, указывающее, какой тип распределителя используется.</span><span class="sxs-lookup"><span data-stu-id="90aed-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90aed-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90aed-109">Return value</span></span>

<span data-ttu-id="90aed-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="90aed-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90aed-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90aed-111">Remarks</span></span>

<span data-ttu-id="90aed-112">Фильтр-владелец должен вызвать этот метод после того, как ПИН-коды согласны с распределителем.</span><span class="sxs-lookup"><span data-stu-id="90aed-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="90aed-113">Если фильтр знает, что распределитель является объектом **Цимажеаллокатор** , он должен вызвать этот метод со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="90aed-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="90aed-114">(Как правило, фильтр будет узнавать это только в том случае, если он владеет этим распределителем.) В противном случае он должен вызвать этот метод со значением **false**.</span><span class="sxs-lookup"><span data-stu-id="90aed-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="90aed-115">Требования</span><span class="sxs-lookup"><span data-stu-id="90aed-115">Requirements</span></span>



| <span data-ttu-id="90aed-116">Требование</span><span class="sxs-lookup"><span data-stu-id="90aed-116">Requirement</span></span> | <span data-ttu-id="90aed-117">Значение</span><span class="sxs-lookup"><span data-stu-id="90aed-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90aed-118">Header</span><span class="sxs-lookup"><span data-stu-id="90aed-118">Header</span></span><br/>  | <dl> <span data-ttu-id="90aed-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90aed-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90aed-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90aed-120">Library</span></span><br/> | <dl> <span data-ttu-id="90aed-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="90aed-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90aed-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90aed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90aed-123">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="90aed-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="90aed-124">**Кдравимаже::D Равимаже**</span><span class="sxs-lookup"><span data-stu-id="90aed-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 





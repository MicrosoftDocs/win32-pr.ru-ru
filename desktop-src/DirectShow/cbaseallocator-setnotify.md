---
description: 'Метод Сетнотифи задает или удаляет обратный вызов для распределителя. Распределитель вызывает метод обратного вызова при вызове метода распределителя Имемаллокатор:: Релеасебуффер.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Кбасеаллокатор. Сетнотифи, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657850"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="673ee-104">Кбасеаллокатор. Сетнотифи, метод</span><span class="sxs-lookup"><span data-stu-id="673ee-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="673ee-105">\[[**Сетнотифи**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) может быть изменен или недоступен в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="673ee-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="673ee-106">`SetNotify`Метод задает или удаляет обратный вызов для распределителя.</span><span class="sxs-lookup"><span data-stu-id="673ee-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="673ee-107">Распределитель вызывает метод обратного вызова при вызове метода распределителя [**имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="673ee-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="673ee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="673ee-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="673ee-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="673ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673ee-110">*пнотифи*</span><span class="sxs-lookup"><span data-stu-id="673ee-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="673ee-111">Указатель на интерфейс [**имемаллокаторнотификаллбакктемп**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) , который будет использоваться для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="673ee-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="673ee-112">Вызывающий объект должен реализовать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="673ee-112">The caller must implement the interface.</span></span> <span data-ttu-id="673ee-113">Чтобы удалить обратный вызов, используйте значение **null** .</span><span class="sxs-lookup"><span data-stu-id="673ee-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673ee-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="673ee-114">Return value</span></span>

<span data-ttu-id="673ee-115">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="673ee-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="673ee-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="673ee-116">Remarks</span></span>

<span data-ttu-id="673ee-117">Этот метод реализует метод [**имемаллокаторкаллбакктемп:: сетнотифи**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) .</span><span class="sxs-lookup"><span data-stu-id="673ee-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="673ee-118">Распределитель не предоставляет интерфейс [**имемаллокаторкаллбакктемп**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , если в конструкторе [**кбасеаллокатор**](cbaseallocator.md) для флага *Фенаблерелеасекаллбакк* не задано **значение true** .</span><span class="sxs-lookup"><span data-stu-id="673ee-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="673ee-119">Этот метод задает переменную члена [**кбасеаллокатор:: m \_ пнотифи**](cbaseallocator-m-pnotify.md) равную *пнотифи* и увеличивает счетчик ссылок в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="673ee-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="673ee-120">Если *значение \_ m Пнотифи* не **равно NULL**, метод **Релеасебуффер** распределителя вызывает [**имемаллокаторнотификаллбакктемп:: нотифирелеасе**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span><span class="sxs-lookup"><span data-stu-id="673ee-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="673ee-121">Сведения о реализации обратного вызова см. в подразделе "Примечания" этого метода.</span><span class="sxs-lookup"><span data-stu-id="673ee-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="673ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="673ee-122">Requirements</span></span>



| <span data-ttu-id="673ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="673ee-123">Requirement</span></span> | <span data-ttu-id="673ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="673ee-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673ee-125">Header</span><span class="sxs-lookup"><span data-stu-id="673ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="673ee-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="673ee-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="673ee-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="673ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="673ee-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="673ee-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673ee-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="673ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673ee-130">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="673ee-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





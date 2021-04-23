---
description: Метод Креатеимажесампле создает пример носителя.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Цимажеаллокатор. Креатеимажесампле, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657542"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="f103d-103">Цимажеаллокатор. Креатеимажесампле, метод</span><span class="sxs-lookup"><span data-stu-id="f103d-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="f103d-104">`CreateImageSample`Метод создает пример носителя.</span><span class="sxs-lookup"><span data-stu-id="f103d-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f103d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f103d-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="f103d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f103d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f103d-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="f103d-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f103d-108">Указатель на буфер *длины* размера, выделенный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="f103d-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="f103d-109">*Длина*</span><span class="sxs-lookup"><span data-stu-id="f103d-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="f103d-110">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="f103d-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f103d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f103d-111">Return value</span></span>

<span data-ttu-id="f103d-112">Возвращает объект [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="f103d-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f103d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f103d-113">Remarks</span></span>

<span data-ttu-id="f103d-114">Этот метод создает образец носителя, реализованный как объект **Цимажесампле** .</span><span class="sxs-lookup"><span data-stu-id="f103d-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="f103d-115">Метод [**имедиасампле::-Point**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) в примере возвращает указатель на буфер, указанный в параметре *pData* .</span><span class="sxs-lookup"><span data-stu-id="f103d-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="f103d-116">Если вы наследуете новый класс распределителя из [**Цимажеаллокатор**](cimageallocator.md) и новый пример класса Media из [**Цимажесампле**](cimagesample.md), следует переопределить этот метод, чтобы создать экземпляр класса-примера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f103d-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f103d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f103d-117">Requirements</span></span>



| <span data-ttu-id="f103d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f103d-118">Requirement</span></span> | <span data-ttu-id="f103d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f103d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f103d-120">Header</span><span class="sxs-lookup"><span data-stu-id="f103d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f103d-121"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f103d-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f103d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f103d-122">Library</span></span><br/> | <dl> <span data-ttu-id="f103d-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f103d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f103d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f103d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f103d-125">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="f103d-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="f103d-126">**Цимажеаллокатор:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="f103d-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 





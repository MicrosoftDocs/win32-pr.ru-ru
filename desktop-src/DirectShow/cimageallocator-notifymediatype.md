---
description: Метод Нотифимедиатипе информирует объект о текущем типе мультимедиа.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Цимажеаллокатор. Нотифимедиатипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657765"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="f5189-103">Цимажеаллокатор. Нотифимедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="f5189-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="f5189-104">`NotifyMediaType`Метод информирует объект о текущем типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f5189-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5189-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5189-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="f5189-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5189-107">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="f5189-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="f5189-108">Указатель на объект [**кмедиатипе**](cmediatype.md) или **значение NULL** для очистки типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f5189-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5189-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5189-109">Return value</span></span>

<span data-ttu-id="f5189-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f5189-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5189-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5189-111">Remarks</span></span>

<span data-ttu-id="f5189-112">Фильтр-владелец должен вызывать этот метод при каждом изменении типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f5189-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="f5189-113">Обычно это происходит, когда ПИН-код сначала соединяется и после динамического изменения формата.</span><span class="sxs-lookup"><span data-stu-id="f5189-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="f5189-114">Распределитель использует тип носителя для проверки предложенных свойств распределителя, а также при создании образцов носителя.</span><span class="sxs-lookup"><span data-stu-id="f5189-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="f5189-115">Объект **Цимажеаллокатор** сохраняет указатель *пмедиатипе* в переменной элемента **m \_ пмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="f5189-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="f5189-116">Таким образом, если вызывающему объекту нужно освободить объект **кмедиатипе** , он должен обновить распределитель путем повторного вызова этого метода либо с новым указателем, либо со значением **null** .</span><span class="sxs-lookup"><span data-stu-id="f5189-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="f5189-117">В противном случае при попытке распределителя ссылаться на старый указатель может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="f5189-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5189-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f5189-118">Requirements</span></span>



| <span data-ttu-id="f5189-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f5189-119">Requirement</span></span> | <span data-ttu-id="f5189-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f5189-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5189-121">Header</span><span class="sxs-lookup"><span data-stu-id="f5189-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f5189-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5189-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5189-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5189-123">Library</span></span><br/> | <dl> <span data-ttu-id="f5189-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f5189-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5189-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5189-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5189-126">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="f5189-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 





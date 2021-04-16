---
description: Метод Нотифимедиатипе уведомляет объект Кдравимаже о текущем типе мультимедиа.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Кдравимаже. Нотифимедиатипе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679762"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="b8f38-103">Кдравимаже. Нотифимедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="b8f38-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="b8f38-104">`NotifyMediaType`Метод уведомляет объект **кдравимаже** текущего типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8f38-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f38-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="b8f38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f38-107">*пмедиатипе*</span><span class="sxs-lookup"><span data-stu-id="b8f38-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f38-108">Указатель на объект [**кмедиатипе**](cmediatype.md) или **значение NULL** для очистки типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8f38-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f38-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8f38-109">Return value</span></span>

<span data-ttu-id="b8f38-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8f38-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f38-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f38-111">Remarks</span></span>

<span data-ttu-id="b8f38-112">Фильтр-владелец должен вызывать этот метод при каждом изменении типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b8f38-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="b8f38-113">Обычно это происходит, когда ПИН-код сначала соединяется и после динамического изменения формата.</span><span class="sxs-lookup"><span data-stu-id="b8f38-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="b8f38-114">Объект **кдравимаже** сохраняет указатель *пмедиатипе* в переменной элемента **m \_ пмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="b8f38-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="b8f38-115">Таким образом, если вызывающему объекту нужно освободить объект **кмедиатипе** , он должен обновить объект **кдравимаже** , вызвав этот метод еще раз, либо с новым указателем, либо со значением **null** .</span><span class="sxs-lookup"><span data-stu-id="b8f38-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="b8f38-116">В противном случае ошибка может возникнуть, когда объект **кдравимаже** пытается сослаться на старый указатель.</span><span class="sxs-lookup"><span data-stu-id="b8f38-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f38-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f38-117">Requirements</span></span>



| <span data-ttu-id="b8f38-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f38-118">Requirement</span></span> | <span data-ttu-id="b8f38-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f38-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f38-120">Header</span><span class="sxs-lookup"><span data-stu-id="b8f38-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b8f38-121"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8f38-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8f38-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8f38-122">Library</span></span><br/> | <dl> <span data-ttu-id="b8f38-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b8f38-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f38-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f38-125">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="b8f38-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





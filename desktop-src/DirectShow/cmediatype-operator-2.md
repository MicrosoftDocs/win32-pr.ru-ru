---
description: Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h) — параметр мтипе'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389040"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="6fe53-103">Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h)</span><span class="sxs-lookup"><span data-stu-id="6fe53-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="6fe53-104">Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6fe53-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fe53-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="6fe53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fe53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe53-107">*мтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="6fe53-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe53-108">Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="6fe53-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe53-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fe53-109">Return value</span></span>

<span data-ttu-id="6fe53-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="6fe53-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe53-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6fe53-111">Requirements</span></span>



| <span data-ttu-id="6fe53-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6fe53-112">Requirement</span></span> | <span data-ttu-id="6fe53-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6fe53-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe53-114">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6fe53-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6fe53-115"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fe53-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6fe53-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6fe53-116">Library</span></span><br/> | <dl> <span data-ttu-id="6fe53-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6fe53-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe53-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6fe53-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe53-119">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="6fe53-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





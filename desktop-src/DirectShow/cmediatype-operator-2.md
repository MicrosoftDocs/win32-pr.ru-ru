---
description: Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h)'
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
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689288"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="76673-103">Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h)</span><span class="sxs-lookup"><span data-stu-id="76673-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="76673-104">Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="76673-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="76673-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76673-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="76673-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76673-107">*мтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="76673-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="76673-108">Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="76673-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76673-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76673-109">Return value</span></span>

<span data-ttu-id="76673-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="76673-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="76673-111">Требования</span><span class="sxs-lookup"><span data-stu-id="76673-111">Requirements</span></span>



| <span data-ttu-id="76673-112">Требование</span><span class="sxs-lookup"><span data-stu-id="76673-112">Requirement</span></span> | <span data-ttu-id="76673-113">Значение</span><span class="sxs-lookup"><span data-stu-id="76673-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76673-114">Header</span><span class="sxs-lookup"><span data-stu-id="76673-114">Header</span></span><br/>  | <dl> <span data-ttu-id="76673-115"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76673-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="76673-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76673-116">Library</span></span><br/> | <dl> <span data-ttu-id="76673-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="76673-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76673-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76673-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76673-119">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="76673-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





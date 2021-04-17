---
description: 'Метод Кмедиатипе. Кмедиатипе:: operator = (Мтипе. h) перегружает оператор присваивания для копирования типа мультимедиа.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h) — параметр кмтипе'
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
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674777"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="96a84-103">Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h) — параметр кмтипе</span><span class="sxs-lookup"><span data-stu-id="96a84-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="96a84-104">Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="96a84-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96a84-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="96a84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96a84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a84-107">*кмтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="96a84-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="96a84-108">Ссылка на объект **кмедиатипе** .</span><span class="sxs-lookup"><span data-stu-id="96a84-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a84-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96a84-109">Return value</span></span>

<span data-ttu-id="96a84-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="96a84-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a84-111">Требования</span><span class="sxs-lookup"><span data-stu-id="96a84-111">Requirements</span></span>

| <span data-ttu-id="96a84-112">Требование</span><span class="sxs-lookup"><span data-stu-id="96a84-112">Requirement</span></span>                   | <span data-ttu-id="96a84-113">Значение</span><span class="sxs-lookup"><span data-stu-id="96a84-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a84-114">Header</span><span class="sxs-lookup"><span data-stu-id="96a84-114">Header</span></span>  | <span data-ttu-id="96a84-115">Мтипе. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="96a84-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="96a84-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96a84-116">Library</span></span> | <span data-ttu-id="96a84-117">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="96a84-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="96a84-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96a84-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a84-119">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="96a84-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





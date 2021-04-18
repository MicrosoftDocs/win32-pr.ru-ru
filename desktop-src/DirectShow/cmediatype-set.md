---
description: Метод Кмедиатипе. Set (Мтипе. h) задает тип носителя с другого типа носителя. Метод использует параметр "кмтипе".
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Метод Кмедиатипе. Set (Мтипе. h) — кмтипе [ref]
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105665017"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="6a80e-104">Метод Кмедиатипе. Set (Мтипе. h) — кмтипе [ref]</span><span class="sxs-lookup"><span data-stu-id="6a80e-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="6a80e-105">`Set`Метод задает тип мультимедиа из другого типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6a80e-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a80e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a80e-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="6a80e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a80e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a80e-108">*кмтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="6a80e-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6a80e-109">Ссылка на объект [**кмедиатипе**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a80e-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a80e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a80e-110">Return value</span></span>

<span data-ttu-id="6a80e-111">Возвращает S \_ OK или E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6a80e-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a80e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a80e-112">Remarks</span></span>

<span data-ttu-id="6a80e-113">Этот метод копирует весь тип мультимедиа из *кмтипе*.</span><span class="sxs-lookup"><span data-stu-id="6a80e-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a80e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6a80e-114">Requirements</span></span>

| <span data-ttu-id="6a80e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6a80e-115">Requirement</span></span>                   | <span data-ttu-id="6a80e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6a80e-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a80e-117">Header</span><span class="sxs-lookup"><span data-stu-id="6a80e-117">Header</span></span>  | <span data-ttu-id="6a80e-118">Мтипе. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="6a80e-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="6a80e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6a80e-119">Library</span></span> | <span data-ttu-id="6a80e-120">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="6a80e-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="6a80e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a80e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a80e-122">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="6a80e-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





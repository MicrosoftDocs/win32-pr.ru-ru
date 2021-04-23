---
description: Сведения о методе Кмедиатипе. Кмедиатипе (Мтипе. h). Этот метод использует параметр "мажортипе".
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметр мажортипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674770"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="27b52-104">Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметр мажортипе</span><span class="sxs-lookup"><span data-stu-id="27b52-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="27b52-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="27b52-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b52-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27b52-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="27b52-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b52-108">*мажортипе*</span><span class="sxs-lookup"><span data-stu-id="27b52-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="27b52-109">Указатель на **идентификатор GUID** основного типа.</span><span class="sxs-lookup"><span data-stu-id="27b52-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="27b52-110">Конструктор инициализирует это значение GUID основного типа.</span><span class="sxs-lookup"><span data-stu-id="27b52-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27b52-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27b52-111">Remarks</span></span>

<span data-ttu-id="27b52-112">Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="27b52-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b52-113">Требования</span><span class="sxs-lookup"><span data-stu-id="27b52-113">Requirements</span></span>

| <span data-ttu-id="27b52-114">Требование</span><span class="sxs-lookup"><span data-stu-id="27b52-114">Requirement</span></span>                   | <span data-ttu-id="27b52-115">Значение</span><span class="sxs-lookup"><span data-stu-id="27b52-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b52-116">Header</span><span class="sxs-lookup"><span data-stu-id="27b52-116">Header</span></span>  | <span data-ttu-id="27b52-117">Мтипе. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="27b52-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="27b52-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27b52-118">Library</span></span> | <span data-ttu-id="27b52-119">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="27b52-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="27b52-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27b52-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b52-121">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="27b52-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





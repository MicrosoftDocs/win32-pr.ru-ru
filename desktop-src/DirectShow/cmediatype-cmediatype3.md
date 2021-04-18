---
description: Сведения о методе Кмедиатипе. Кмедиатипе (Мтипе. h). Этот метод использует параметры "мтипе" и "фр".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры мтипе и фр
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105665019"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="c8704-104">Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры мтипе и фр</span><span class="sxs-lookup"><span data-stu-id="c8704-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="c8704-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c8704-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8704-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8704-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c8704-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8704-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8704-108">*мтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="c8704-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c8704-109">Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c8704-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="c8704-110">Конструктор копирует тип мультимедиа в новый объект, включая блок формата, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="c8704-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="c8704-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="c8704-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c8704-112">Указатель на переменную, которая получает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c8704-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="c8704-113">Этот параметр может быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="c8704-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="c8704-114">В противном случае перед вызовом конструктора вызывающий объект должен установить значение, равное « \_ ОК».</span><span class="sxs-lookup"><span data-stu-id="c8704-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="c8704-115">Если конструктор завершается неудачно, ему присваивается значение кода сбоя.</span><span class="sxs-lookup"><span data-stu-id="c8704-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8704-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8704-116">Remarks</span></span>

<span data-ttu-id="c8704-117">Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c8704-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8704-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c8704-118">Requirements</span></span>

| <span data-ttu-id="c8704-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c8704-119">Requirement</span></span>                   | <span data-ttu-id="c8704-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c8704-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8704-121">Header</span><span class="sxs-lookup"><span data-stu-id="c8704-121">Header</span></span>  | <span data-ttu-id="c8704-122">Мтипе. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c8704-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c8704-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8704-123">Library</span></span> | <span data-ttu-id="c8704-124">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="c8704-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c8704-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8704-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8704-126">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c8704-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





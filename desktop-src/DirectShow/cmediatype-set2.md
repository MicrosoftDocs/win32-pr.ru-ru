---
description: Метод Set задает тип мультимедиа из другого типа носителя.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Метод Кмедиатипе. Set (Мтипе. h)
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
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665297"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="36432-103">Метод Кмедиатипе. Set (Мтипе. h)</span><span class="sxs-lookup"><span data-stu-id="36432-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="36432-104">`Set`Метод задает тип мультимедиа из другого типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="36432-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="36432-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36432-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="36432-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36432-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36432-107">*мтипе* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="36432-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="36432-108">Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="36432-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36432-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36432-109">Return value</span></span>

<span data-ttu-id="36432-110">Возвращает S \_ OK или E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="36432-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="36432-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36432-111">Remarks</span></span>

<span data-ttu-id="36432-112">Этот метод копирует весь тип мультимедиа из *мтипе*.</span><span class="sxs-lookup"><span data-stu-id="36432-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="36432-113">Требования</span><span class="sxs-lookup"><span data-stu-id="36432-113">Requirements</span></span>



| <span data-ttu-id="36432-114">Требование</span><span class="sxs-lookup"><span data-stu-id="36432-114">Requirement</span></span> | <span data-ttu-id="36432-115">Значение</span><span class="sxs-lookup"><span data-stu-id="36432-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36432-116">Header</span><span class="sxs-lookup"><span data-stu-id="36432-116">Header</span></span><br/>  | <dl> <span data-ttu-id="36432-117"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36432-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="36432-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36432-118">Library</span></span><br/> | <dl> <span data-ttu-id="36432-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="36432-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36432-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36432-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36432-121">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="36432-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





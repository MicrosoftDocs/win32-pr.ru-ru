---
description: Функция Креатемедиатипе выделяет новую \_ \_ структуру типа мультимедиа am, включая блок Format.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Функция Креатемедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679677"
---
# <a name="createmediatype-function"></a><span data-ttu-id="c7569-103">Функция Креатемедиатипе</span><span class="sxs-lookup"><span data-stu-id="c7569-103">CreateMediaType function</span></span>

<span data-ttu-id="c7569-104">Функция **креатемедиатипе** выделяет новую структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , включая блок Format.</span><span class="sxs-lookup"><span data-stu-id="c7569-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7569-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7569-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="c7569-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7569-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7569-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="c7569-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="c7569-108">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c7569-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="c7569-109">Метод копирует эту структуру в новую структуру.</span><span class="sxs-lookup"><span data-stu-id="c7569-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7569-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7569-110">Return value</span></span>

<span data-ttu-id="c7569-111">Возвращает новую структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) или **значение NULL** , если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7569-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7569-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7569-112">Remarks</span></span>

<span data-ttu-id="c7569-113">Чтобы освободить память, выделенную этой функцией, вызовите [**делетемедиатипе**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="c7569-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7569-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c7569-114">Requirements</span></span>



| <span data-ttu-id="c7569-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c7569-115">Requirement</span></span> | <span data-ttu-id="c7569-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c7569-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7569-117">Header</span><span class="sxs-lookup"><span data-stu-id="c7569-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c7569-118"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7569-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c7569-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7569-119">Library</span></span><br/> | <dl> <span data-ttu-id="c7569-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c7569-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7569-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7569-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7569-122">**Функции типа мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="c7569-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 





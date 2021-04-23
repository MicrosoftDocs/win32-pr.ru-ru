---
description: Функция Фримедиатипе удаляет блок формата в \_ \_ структуре типа мультимедиа AM.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Функция Фримедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679689"
---
# <a name="freemediatype-function"></a><span data-ttu-id="06239-103">Функция Фримедиатипе</span><span class="sxs-lookup"><span data-stu-id="06239-103">FreeMediaType function</span></span>

<span data-ttu-id="06239-104">Функция **фримедиатипе** удаляет блок формата в структуре [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="06239-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="06239-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06239-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="06239-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06239-107">*MT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="06239-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="06239-108">Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="06239-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06239-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06239-109">Return value</span></span>

<span data-ttu-id="06239-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="06239-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06239-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06239-111">Remarks</span></span>

<span data-ttu-id="06239-112">Блок формата выделяется в куче.</span><span class="sxs-lookup"><span data-stu-id="06239-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="06239-113">Элемент **пбформат** [**\_ \_ типа носителя AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) указывает на блок формата.</span><span class="sxs-lookup"><span data-stu-id="06239-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="06239-114">Используйте эту функцию, чтобы освободить только блок формата.</span><span class="sxs-lookup"><span data-stu-id="06239-114">Use this function to free just the format block.</span></span> <span data-ttu-id="06239-115">Чтобы удалить выделенную **структуру \_ \_ типа носителя** , вызовите [**делетемедиатипе**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="06239-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="06239-116">Эта функция определена в библиотеке [базовых классов DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="06239-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="06239-117">Если вы предпочитаете не ссылаться на библиотеку базовых классов, можно использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="06239-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="06239-118">Требования</span><span class="sxs-lookup"><span data-stu-id="06239-118">Requirements</span></span>



| <span data-ttu-id="06239-119">Требование</span><span class="sxs-lookup"><span data-stu-id="06239-119">Requirement</span></span> | <span data-ttu-id="06239-120">Значение</span><span class="sxs-lookup"><span data-stu-id="06239-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06239-121">Header</span><span class="sxs-lookup"><span data-stu-id="06239-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06239-122"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06239-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="06239-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06239-123">Library</span></span><br/> | <dl> <span data-ttu-id="06239-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="06239-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06239-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06239-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06239-126">**делетемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="06239-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="06239-127">**Функции типа мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="06239-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 





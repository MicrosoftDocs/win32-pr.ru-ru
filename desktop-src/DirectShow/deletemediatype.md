---
description: Функция Делетемедиатипе удаляет выделенную \_ \_ структуру типа файлов am, включая блок Format.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Функция Делетемедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657097"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="321d9-103">Функция Делетемедиатипе</span><span class="sxs-lookup"><span data-stu-id="321d9-103">DeleteMediaType function</span></span>

<span data-ttu-id="321d9-104">Функция **делетемедиатипе** удаляет выделенную структуру [**\_ \_ типа файлов AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , включая блок Format.</span><span class="sxs-lookup"><span data-stu-id="321d9-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="321d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="321d9-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="321d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="321d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321d9-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="321d9-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="321d9-108">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="321d9-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321d9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="321d9-109">Return value</span></span>

<span data-ttu-id="321d9-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="321d9-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="321d9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="321d9-111">Remarks</span></span>

<span data-ttu-id="321d9-112">Эта функция используется для освобождения любой структуры типа мультимедиа, выделенной с помощью инструкции [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) или [**креатемедиатипе**](createmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="321d9-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="321d9-113">Эта функция определена в библиотеке [базовых классов DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="321d9-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="321d9-114">Если вы предпочитаете не ссылаться на библиотеку базовых классов, можно использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="321d9-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


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


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="321d9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="321d9-115">Requirements</span></span>



| <span data-ttu-id="321d9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="321d9-116">Requirement</span></span> | <span data-ttu-id="321d9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="321d9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321d9-118">Header</span><span class="sxs-lookup"><span data-stu-id="321d9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="321d9-119"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="321d9-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="321d9-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="321d9-120">Library</span></span><br/> | <dl> <span data-ttu-id="321d9-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="321d9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321d9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="321d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321d9-123">**фримедиатипе**</span><span class="sxs-lookup"><span data-stu-id="321d9-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="321d9-124">**Функции типа мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="321d9-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 


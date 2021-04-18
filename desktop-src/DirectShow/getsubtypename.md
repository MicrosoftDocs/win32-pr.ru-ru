---
description: Функция Жетсубтипенаме извлекает удобное для восприятия имя подтипа видео.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Функция Жетсубтипенаме (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652108"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="6019c-103">Функция Жетсубтипенаме</span><span class="sxs-lookup"><span data-stu-id="6019c-103">GetSubtypeName function</span></span>

<span data-ttu-id="6019c-104">`GetSubtypeName`Функция получает удобное для восприятия имя подтипа видео.</span><span class="sxs-lookup"><span data-stu-id="6019c-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="6019c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6019c-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="6019c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6019c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6019c-107">*псубтипе*</span><span class="sxs-lookup"><span data-stu-id="6019c-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="6019c-108">Указатель на **GUID** подтипа видео.</span><span class="sxs-lookup"><span data-stu-id="6019c-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6019c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6019c-109">Return value</span></span>

<span data-ttu-id="6019c-110">Возвращает строку, содержащую имя.</span><span class="sxs-lookup"><span data-stu-id="6019c-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="6019c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6019c-111">Requirements</span></span>



| <span data-ttu-id="6019c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6019c-112">Requirement</span></span> | <span data-ttu-id="6019c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6019c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6019c-114">Header</span><span class="sxs-lookup"><span data-stu-id="6019c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6019c-115"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6019c-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6019c-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6019c-116">Library</span></span><br/> | <dl> <span data-ttu-id="6019c-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6019c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6019c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6019c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6019c-119">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="6019c-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





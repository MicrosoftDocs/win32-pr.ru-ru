---
description: Метод Матчеспартиал определяет, соответствует ли этот тип носителя частично указанному типу носителя.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Кмедиатипе. Матчеспартиал, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668981"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="40ebd-103">Кмедиатипе. Матчеспартиал, метод</span><span class="sxs-lookup"><span data-stu-id="40ebd-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="40ebd-104">`MatchesPartial`Метод определяет, соответствует ли этот тип носителя частично указанному типу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="40ebd-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ebd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40ebd-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="40ebd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="40ebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ebd-107">*ппартиал*</span><span class="sxs-lookup"><span data-stu-id="40ebd-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="40ebd-108">Указатель на тип носителя для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="40ebd-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ebd-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40ebd-109">Return value</span></span>

<span data-ttu-id="40ebd-110">Возвращает **значение true** , если типы мультимедиа совпадают.</span><span class="sxs-lookup"><span data-stu-id="40ebd-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="40ebd-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="40ebd-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ebd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40ebd-112">Remarks</span></span>

<span data-ttu-id="40ebd-113">Тип носителя, заданный параметром *ппартиал* , может иметь значение GUID \_ null для основного типа, подтипа или типа формата.</span><span class="sxs-lookup"><span data-stu-id="40ebd-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="40ebd-114">Все элементы со \_ значениями NULL GUID не проверяются.</span><span class="sxs-lookup"><span data-stu-id="40ebd-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="40ebd-115">(По сути, GUID \_ NULL выступает в качестве подстановочного знака.) Элементы со значениями, отличными от GUID \_ null, должны соответствовать типу носителя.</span><span class="sxs-lookup"><span data-stu-id="40ebd-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ebd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="40ebd-116">Requirements</span></span>



| <span data-ttu-id="40ebd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="40ebd-117">Requirement</span></span> | <span data-ttu-id="40ebd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="40ebd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ebd-119">Header</span><span class="sxs-lookup"><span data-stu-id="40ebd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="40ebd-120"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40ebd-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="40ebd-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="40ebd-121">Library</span></span><br/> | <dl> <span data-ttu-id="40ebd-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="40ebd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ebd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40ebd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ebd-124">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="40ebd-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





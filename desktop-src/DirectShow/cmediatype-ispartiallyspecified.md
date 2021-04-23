---
description: Метод ИспартиаллиспеЦифиед определяет, определен ли тип мультимедиа частично. Тип мультимедиа является разделяемым, если основной тип, подтип или тип формата имеют \_ значение GUID null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Кмедиатипе. ИспартиаллиспеЦифиед, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676010"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="89732-104">Кмедиатипе. ИспартиаллиспеЦифиед, метод</span><span class="sxs-lookup"><span data-stu-id="89732-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="89732-105">`IsPartiallySpecified`Метод определяет, определен ли тип мультимедиа частично.</span><span class="sxs-lookup"><span data-stu-id="89732-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="89732-106">Тип мультимедиа является *разделяемым* , если основной тип, подтип или тип формата имеют \_ значение GUID null.</span><span class="sxs-lookup"><span data-stu-id="89732-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="89732-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89732-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="89732-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89732-108">Parameters</span></span>

<span data-ttu-id="89732-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="89732-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89732-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89732-110">Return value</span></span>

<span data-ttu-id="89732-111">Возвращает **значение true** , если тип мультимедиа указан частично.</span><span class="sxs-lookup"><span data-stu-id="89732-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="89732-112">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="89732-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89732-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89732-113">Remarks</span></span>

<span data-ttu-id="89732-114">Метод [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) может принимать частичные типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="89732-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="89732-115">Реализация фактически не тестирует подтип.</span><span class="sxs-lookup"><span data-stu-id="89732-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="89732-116">Если существует указанный тип формата, тип мультимедиа не считается частичным, даже если его подтип имеет \_ значение GUID null.</span><span class="sxs-lookup"><span data-stu-id="89732-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="89732-117">Требования</span><span class="sxs-lookup"><span data-stu-id="89732-117">Requirements</span></span>



| <span data-ttu-id="89732-118">Требование</span><span class="sxs-lookup"><span data-stu-id="89732-118">Requirement</span></span> | <span data-ttu-id="89732-119">Значение</span><span class="sxs-lookup"><span data-stu-id="89732-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89732-120">Header</span><span class="sxs-lookup"><span data-stu-id="89732-120">Header</span></span><br/>  | <dl> <span data-ttu-id="89732-121"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89732-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="89732-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89732-122">Library</span></span><br/> | <dl> <span data-ttu-id="89732-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89732-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89732-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89732-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89732-125">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="89732-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





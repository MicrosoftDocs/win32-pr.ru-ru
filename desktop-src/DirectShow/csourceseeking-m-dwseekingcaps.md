---
description: Поиск возможностей.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Элемент Ксаурцесикинг:: m_dwSeekingCaps (Ктлутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657496"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="a63d3-103">Элемент Ксаурцесикинг:: m \_ двсикингкапс</span><span class="sxs-lookup"><span data-stu-id="a63d3-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="a63d3-104">Поиск возможностей.</span><span class="sxs-lookup"><span data-stu-id="a63d3-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a63d3-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="a63d3-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="a63d3-106">Remarks</span></span>

<span data-ttu-id="a63d3-107">По умолчанию для этого параметра задано побитовое сочетание следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="a63d3-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="a63d3-108">\_Поиск \_ кансикфорвардс</span><span class="sxs-lookup"><span data-stu-id="a63d3-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="a63d3-109">\_Поиск \_ кансикбакквардс</span><span class="sxs-lookup"><span data-stu-id="a63d3-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="a63d3-110">\_Поиск \_ кансикабсолуте</span><span class="sxs-lookup"><span data-stu-id="a63d3-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="a63d3-111">\_Поиск \_ канжетстоппос</span><span class="sxs-lookup"><span data-stu-id="a63d3-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="a63d3-112">\_Поиск \_ канжетдуратион</span><span class="sxs-lookup"><span data-stu-id="a63d3-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="a63d3-113">Если фильтр поддерживает другой набор возможностей, Переопределите это значение.</span><span class="sxs-lookup"><span data-stu-id="a63d3-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63d3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a63d3-114">Requirements</span></span>



| <span data-ttu-id="a63d3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a63d3-115">Requirement</span></span> | <span data-ttu-id="a63d3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a63d3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a63d3-117">Header</span><span class="sxs-lookup"><span data-stu-id="a63d3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a63d3-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a63d3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a63d3-119">Library</span></span><br/> | <dl> <span data-ttu-id="a63d3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63d3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a63d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63d3-122">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="a63d3-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





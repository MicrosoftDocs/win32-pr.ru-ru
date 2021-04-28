---
description: 'Ктрансформаутпутпин:: m_pPosition элемент вспомогательного объекта для передачи команд поиска в восходящий поток.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Элемент Ктрансформаутпутпин:: m_pPosition (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084862"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="2ac96-103">Элемент Ктрансформаутпутпин:: m \_ ппоситион</span><span class="sxs-lookup"><span data-stu-id="2ac96-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="2ac96-104">Вспомогательный объект для передачи команд поиска в восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="2ac96-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ac96-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="2ac96-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ac96-106">Remarks</span></span>

<span data-ttu-id="2ac96-107">Когда ПИН-код сначала запрашивает интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) или [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , он создает и выполняет статистическую обработку объекта вспомогательного приложения [**кпоспасссру**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="2ac96-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac96-108">Требования</span><span class="sxs-lookup"><span data-stu-id="2ac96-108">Requirements</span></span>



| <span data-ttu-id="2ac96-109">Требование</span><span class="sxs-lookup"><span data-stu-id="2ac96-109">Requirement</span></span> | <span data-ttu-id="2ac96-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2ac96-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac96-111">Header</span><span class="sxs-lookup"><span data-stu-id="2ac96-111">Header</span></span><br/>  | <dl> <span data-ttu-id="2ac96-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac96-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ac96-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ac96-113">Library</span></span><br/> | <dl> <span data-ttu-id="2ac96-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac96-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





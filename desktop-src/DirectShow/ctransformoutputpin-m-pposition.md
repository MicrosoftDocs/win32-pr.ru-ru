---
description: Вспомогательный объект для передачи команд поиска в восходящий поток.
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657726"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="ac94f-103">Элемент Ктрансформаутпутпин:: m \_ ппоситион</span><span class="sxs-lookup"><span data-stu-id="ac94f-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="ac94f-104">Вспомогательный объект для передачи команд поиска в восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="ac94f-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac94f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac94f-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="ac94f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac94f-106">Remarks</span></span>

<span data-ttu-id="ac94f-107">Когда ПИН-код сначала запрашивает интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) или [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , он создает и выполняет статистическую обработку объекта вспомогательного приложения [**кпоспасссру**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="ac94f-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac94f-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ac94f-108">Requirements</span></span>



| <span data-ttu-id="ac94f-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ac94f-109">Requirement</span></span> | <span data-ttu-id="ac94f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ac94f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac94f-111">Header</span><span class="sxs-lookup"><span data-stu-id="ac94f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="ac94f-112"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac94f-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ac94f-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac94f-113">Library</span></span><br/> | <dl> <span data-ttu-id="ac94f-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ac94f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: Функция Думпграф отправляет сведения о графе фильтра в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Функция Думпграф (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652018"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="6066f-104">Функция Думпграф</span><span class="sxs-lookup"><span data-stu-id="6066f-104">DumpGraph function</span></span>

<span data-ttu-id="6066f-105">`DumpGraph`Функция отправляет сведения о графе фильтра в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="6066f-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="6066f-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="6066f-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="6066f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6066f-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="6066f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6066f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6066f-109">*пграф*</span><span class="sxs-lookup"><span data-stu-id="6066f-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="6066f-110">Указатель на интерфейс [**ифилтерграф**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="6066f-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="6066f-111">*двлевел*</span><span class="sxs-lookup"><span data-stu-id="6066f-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="6066f-112">Уровень ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="6066f-112">Logging level.</span></span> <span data-ttu-id="6066f-113">Функция создает \_ сообщение трассировки журнала с указанным уровнем ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="6066f-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6066f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6066f-114">Return value</span></span>

<span data-ttu-id="6066f-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6066f-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6066f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6066f-116">Requirements</span></span>



| <span data-ttu-id="6066f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6066f-117">Requirement</span></span> | <span data-ttu-id="6066f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6066f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6066f-119">Header</span><span class="sxs-lookup"><span data-stu-id="6066f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6066f-120"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6066f-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6066f-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6066f-121">Library</span></span><br/> | <dl> <span data-ttu-id="6066f-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6066f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6066f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6066f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6066f-124">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="6066f-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





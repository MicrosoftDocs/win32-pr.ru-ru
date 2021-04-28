---
description: Метод конструктора Ценумпинс. Ценумпинс.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Конструктор Ценумпинс. Ценумпинс (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099232"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="c4993-103">Ценумпинс. Ценумпинс, конструктор</span><span class="sxs-lookup"><span data-stu-id="c4993-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="c4993-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c4993-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4993-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4993-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="c4993-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4993-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="c4993-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="c4993-108">Указатель на фильтр, по которому производится перечисление ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="c4993-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="c4993-109">*пенумпинс*</span><span class="sxs-lookup"><span data-stu-id="c4993-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="c4993-110">Указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) перечислителя, который необходимо клонировать, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c4993-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4993-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="c4993-111">Remarks</span></span>

<span data-ttu-id="c4993-112">Если *пенумпинс* имеет **значение NULL**, этот метод инициализирует перечислитель до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="c4993-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="c4993-113">В противном случае он дублирует внутреннее состояние перечислителя, заданного параметром *пенумпинс*.</span><span class="sxs-lookup"><span data-stu-id="c4993-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4993-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c4993-114">Requirements</span></span>



| <span data-ttu-id="c4993-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c4993-115">Requirement</span></span> | <span data-ttu-id="c4993-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4993-117">Header</span><span class="sxs-lookup"><span data-stu-id="c4993-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c4993-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4993-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4993-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4993-119">Library</span></span><br/> | <dl> <span data-ttu-id="c4993-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c4993-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4993-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c4993-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4993-122">**Класс Ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="c4993-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 





---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод не использует параметры.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — нет параметров'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674769"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="c641e-104">Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — нет параметров</span><span class="sxs-lookup"><span data-stu-id="c641e-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="c641e-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="c641e-105">Constructor method.</span></span> <span data-ttu-id="c641e-106">Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .</span><span class="sxs-lookup"><span data-stu-id="c641e-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c641e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c641e-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="c641e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c641e-108">Parameters</span></span>

<span data-ttu-id="c641e-109">Этот конструктор не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c641e-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c641e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c641e-110">Remarks</span></span>

<span data-ttu-id="c641e-111">Если этот объект создан с помощью кода **FourCC** , для его сопоставления создается **идентификатор GUID** .</span><span class="sxs-lookup"><span data-stu-id="c641e-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="c641e-112">Если этот объект создается с существующим **идентификатором GUID**, значение **FourCC** объекта устанавливается в 0.</span><span class="sxs-lookup"><span data-stu-id="c641e-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="c641e-113">Впоследствии значение **FourCC** можно задать или получить с помощью функций члена [**сетфауркк**](fourccmap-setfourcc.md) и [**жетфауркк**](fourccmap-getfourcc.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="c641e-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c641e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c641e-114">Requirements</span></span>


| <span data-ttu-id="c641e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c641e-115">Requirement</span></span> | <span data-ttu-id="c641e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c641e-116">Value</span></span> |
|-|-|
| <span data-ttu-id="c641e-117">Header</span><span class="sxs-lookup"><span data-stu-id="c641e-117">Header</span></span>  | <span data-ttu-id="c641e-118">FourCC. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c641e-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="c641e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c641e-119">Library</span></span> | <span data-ttu-id="c641e-120">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="c641e-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="c641e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c641e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c641e-122">**Класс Фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="c641e-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 





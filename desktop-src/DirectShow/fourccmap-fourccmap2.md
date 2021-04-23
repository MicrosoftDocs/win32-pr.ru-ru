---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод использует параметр "FourCC".
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр FourCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105651564"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="a71a7-104">Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр FourCC</span><span class="sxs-lookup"><span data-stu-id="a71a7-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="a71a7-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="a71a7-105">Constructor method.</span></span> <span data-ttu-id="a71a7-106">Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .</span><span class="sxs-lookup"><span data-stu-id="a71a7-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a71a7-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="a71a7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a71a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a71a7-109">*FourCC*</span><span class="sxs-lookup"><span data-stu-id="a71a7-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="a71a7-110">**Параметр DWORD** , указывающий FourCC.</span><span class="sxs-lookup"><span data-stu-id="a71a7-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a71a7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a71a7-111">Remarks</span></span>

<span data-ttu-id="a71a7-112">Если этот объект создан с помощью кода **FourCC** , для его сопоставления создается **идентификатор GUID** .</span><span class="sxs-lookup"><span data-stu-id="a71a7-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="a71a7-113">Если этот объект создается с существующим **идентификатором GUID**, значение **FourCC** объекта устанавливается в 0.</span><span class="sxs-lookup"><span data-stu-id="a71a7-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="a71a7-114">Впоследствии значение **FourCC** можно задать или получить с помощью функций члена [**сетфауркк**](fourccmap-setfourcc.md) и [**жетфауркк**](fourccmap-getfourcc.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="a71a7-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="a71a7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a71a7-115">Requirements</span></span>

| <span data-ttu-id="a71a7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a71a7-116">Requirement</span></span> | <span data-ttu-id="a71a7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a71a7-117">Value</span></span> |
|-|-|
| <span data-ttu-id="a71a7-118">Header</span><span class="sxs-lookup"><span data-stu-id="a71a7-118">Header</span></span>  | <span data-ttu-id="a71a7-119">FourCC. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="a71a7-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="a71a7-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a71a7-120">Library</span></span> | <span data-ttu-id="a71a7-121">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="a71a7-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a71a7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a71a7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71a7-123">**Класс Фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="a71a7-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 





---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод использует параметр "пгуид".
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр пгуид'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674774"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="90622-104">Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр пгуид</span><span class="sxs-lookup"><span data-stu-id="90622-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="90622-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="90622-105">Constructor method.</span></span> <span data-ttu-id="90622-106">Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .</span><span class="sxs-lookup"><span data-stu-id="90622-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="90622-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90622-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="90622-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90622-109">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="90622-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="90622-110">Указатель на глобальный уникальный идентификатор (**GUID**).</span><span class="sxs-lookup"><span data-stu-id="90622-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90622-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90622-111">Remarks</span></span>

<span data-ttu-id="90622-112">Если этот объект создан с помощью кода **FourCC** , для его сопоставления создается **идентификатор GUID** .</span><span class="sxs-lookup"><span data-stu-id="90622-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="90622-113">Если этот объект создается с существующим **идентификатором GUID**, значение **FourCC** объекта устанавливается в 0.</span><span class="sxs-lookup"><span data-stu-id="90622-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="90622-114">Впоследствии значение **FourCC** можно задать или получить с помощью функций члена [**сетфауркк**](fourccmap-setfourcc.md) и [**жетфауркк**](fourccmap-getfourcc.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="90622-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="90622-115">Требования</span><span class="sxs-lookup"><span data-stu-id="90622-115">Requirements</span></span>

| <span data-ttu-id="90622-116">Требование</span><span class="sxs-lookup"><span data-stu-id="90622-116">Requirement</span></span> | <span data-ttu-id="90622-117">Значение</span><span class="sxs-lookup"><span data-stu-id="90622-117">Value</span></span> |
|-|-|
| <span data-ttu-id="90622-118">Header</span><span class="sxs-lookup"><span data-stu-id="90622-118">Header</span></span>  | <span data-ttu-id="90622-119">FourCC. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="90622-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="90622-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90622-120">Library</span></span> | <span data-ttu-id="90622-121">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="90622-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="90622-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90622-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90622-123">**Класс Фаурккмап**</span><span class="sxs-lookup"><span data-stu-id="90622-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 





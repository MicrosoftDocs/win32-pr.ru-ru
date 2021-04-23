---
title: Section
description: Раздел является третьей частью потока набора свойств и содержит фактические значения набора свойств.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661551"
---
# <a name="section"></a><span data-ttu-id="7c9f3-103">Section</span><span class="sxs-lookup"><span data-stu-id="7c9f3-103">Section</span></span>

<span data-ttu-id="7c9f3-104">Раздел является третьей частью потока набора свойств и содержит фактические значения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="7c9f3-105">Раздел содержит:</span><span class="sxs-lookup"><span data-stu-id="7c9f3-105">A section contains:</span></span>

-   <span data-ttu-id="7c9f3-106">Число байтов для раздела, который является инклюзивным от самого числа байтов.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="7c9f3-107">Массив пар ИДЕНТИФИКАТОРов и смещений для 32-битового свойства.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="7c9f3-108">Массив пар "индикатор-значение" типа свойства.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="7c9f3-109">Смещение — это расстояние от начала раздела до начала пары свойство (тип, значение).</span><span class="sxs-lookup"><span data-stu-id="7c9f3-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="7c9f3-110">Это позволяет копировать раздел в виде массива байтов без какого-либо преобразования внутренней структуры.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="7c9f3-111">Следующие псевдо-структуры иллюстрируют формат раздела.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-111">The following pseudo-structures illustrate the format of a section.</span></span>

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 





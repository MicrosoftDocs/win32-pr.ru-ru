---
title: Section
description: Раздел является третьей частью потока набора свойств и содержит фактические значения набора свойств.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682804"
---
# <a name="section"></a>Section

Раздел является третьей частью потока набора свойств и содержит фактические значения набора свойств.

Раздел содержит:

-   Число байтов для раздела, который является инклюзивным от самого числа байтов.
-   Массив пар ИДЕНТИФИКАТОРов и смещений для 32-битового свойства.
-   Массив пар "индикатор-значение" типа свойства.

Смещение — это расстояние от начала раздела до начала пары свойство (тип, значение). Это позволяет копировать раздел в виде массива байтов без какого-либо преобразования внутренней структуры.

Следующие псевдо-структуры иллюстрируют формат раздела.

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

 

 





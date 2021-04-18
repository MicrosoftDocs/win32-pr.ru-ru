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

 

 





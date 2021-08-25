---
title: Перенос функций v
description: В IRI GL для указания вершин используются варианты в функции v. Эквивалентная функция OpenGL Глвертекс ниже — примеры Глвертекс.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Перенос GL в ГК, вершины
- Перенос из IRI GL, вершин
- перенос в OpenGL из IRI GL, вершин
- Перенос по стандарту OpenGL из IRI GL, вершин
- функции рисования, вершины
- вершины, перенос из IRI GL
- Перенос GL в ГК, функции v
- Перенос из функций IRI GL, v
- перенос в OpenGL из функций IRI GL, v
- Перенос по стандарту OpenGL из функций IRI GL, v
- функции рисования, функции v
- функции v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e84fd5eb036afaf5291902ab00f91f3b155f7507d8fce7135dc8030323c1a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888074"
---
# <a name="porting-v-functions"></a>Перенос функций v

В IRI GL для указания вершин используются варианты в функции **v** . Эквивалентная функция OpenGL — [глвертекс](glvertex-functions.md): ниже приведены примеры **глвертекс**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

Функция **глвертекс** использует суффиксы так же, как и другие вызовы OpenGL. Векторные версии вызова принимают массивы соответствующего размера в качестве аргументов. В двумерной версии z = 0 и w = 1. В трехмерной версии w = 1.

 

 





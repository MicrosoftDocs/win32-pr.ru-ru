---
title: Перенос функции bbox2
description: Для функции IRI GL bbox2 не существует эквивалента OpenGL.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Перенос GL в ГК, функция bbox2
- Перенос из IRI GL, функция bbox2
- перенос в OpenGL из IRI GL, функция bbox2
- Перенос по стандарту OpenGL из IRI GL, функция bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012012"
---
# <a name="porting-the-bbox2-function"></a>Перенос функции bbox2

Для функции IRI GL **bbox2** не существует эквивалента OpenGL.

**Перенос кода, содержащего функции bbox2**

1.  Создайте новый список дисплеев (OpenGL), содержащий все в эквивалентном списке дисплеев ДИАФРАГМы, за исключением вызова **bbox2**.
2.  используйте соответствующий код Windows, чтобы нарисовать прямоугольник того же размера, что и для диафрагмы **ббокс** GL.

 

 





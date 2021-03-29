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
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778035"
---
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="90d4d-107">Перенос функции bbox2</span><span class="sxs-lookup"><span data-stu-id="90d4d-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="90d4d-108">Для функции IRI GL **bbox2** не существует эквивалента OpenGL.</span><span class="sxs-lookup"><span data-stu-id="90d4d-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="90d4d-109">**Перенос кода, содержащего функции bbox2**</span><span class="sxs-lookup"><span data-stu-id="90d4d-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="90d4d-110">Создайте новый список дисплеев (OpenGL), содержащий все в эквивалентном списке дисплеев ДИАФРАГМы, за исключением вызова **bbox2**.</span><span class="sxs-lookup"><span data-stu-id="90d4d-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="90d4d-111">Используйте соответствующий код Windows, чтобы нарисовать прямоугольник того же размера, что и **ббокс** GL ГК.</span><span class="sxs-lookup"><span data-stu-id="90d4d-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 





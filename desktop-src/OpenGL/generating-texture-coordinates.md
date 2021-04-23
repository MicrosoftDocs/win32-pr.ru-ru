---
title: Создание координат текстуры
description: Вместо явного предоставления координат текстуры можно создать OpenGL в качестве функции других данных вершин с помощью Глтексжен \.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Конвейер обработки OpenGL, координаты текстуры
- координаты текстуры OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258638"
---
# <a name="generating-texture-coordinates"></a><span data-ttu-id="6d439-105">Создание координат текстуры</span><span class="sxs-lookup"><span data-stu-id="6d439-105">Generating Texture Coordinates</span></span>

<span data-ttu-id="6d439-106">Вместо явного предоставления координат текстуры можно использовать OpenGL для создания их в качестве функции других данных вершин с помощью [глтексжен \* ](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6d439-106">Rather than explicitly supplying texture coordinates, you can have OpenGL generate them as a function of other vertex data using [glTexGen\*](gltexgen-functions.md).</span></span> <span data-ttu-id="6d439-107">После того как координаты текстуры определены или созданы, они преобразуются в матрицу текстуры.</span><span class="sxs-lookup"><span data-stu-id="6d439-107">After the texture coordinates have been specified or generated, they are transformed by the texture matrix.</span></span> <span data-ttu-id="6d439-108">Эта матрица управляется теми же функциями, которые используются для преобразования матриц (см. статью [Преобразование матрицы](matrix-transformations.md)).</span><span class="sxs-lookup"><span data-stu-id="6d439-108">This matrix is controlled with the same functions that are used for matrix transformations (see [Matrix Transformations](matrix-transformations.md)).</span></span>

 

 





---
description: Копирование растрового изображения в параллелограмм; Используйте функцию Плгблт, которая выполняет перенос битового блока из прямоугольника в исходном контексте устройства в параллелограмм в контексте целевого устройства.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Поворот растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997427"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="93b6a-103">Поворот растрового изображения</span><span class="sxs-lookup"><span data-stu-id="93b6a-103">Bitmap Rotation</span></span>

<span data-ttu-id="93b6a-104">Копирование растрового изображения в параллелограмм; Используйте функцию [**плгблт**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , которая выполняет перенос битового блока из прямоугольника в исходном контексте устройства в параллелограмм в контексте целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="93b6a-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="93b6a-105">Чтобы повернуть точечный рисунок, приложение должно предоставить координаты в мировых единицах, которые будут использоваться для углов параллелограмма.</span><span class="sxs-lookup"><span data-stu-id="93b6a-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="93b6a-106">(Дополнительные сведения о повороте и мировых единицах см. в разделе [координатные пространства и преобразования](coordinate-spaces-and-transformations.md).)</span><span class="sxs-lookup"><span data-stu-id="93b6a-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 




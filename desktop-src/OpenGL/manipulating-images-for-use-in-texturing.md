---
title: Обработка изображений для использования в текстурировании
description: Библиотека служебной программы OpenGL (GLU) обеспечивает масштабирование изображений и автоматическое выполнение функций функции текстурирования для упрощения спецификации изображений текстур.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Служебная программа OpenGL (GLU), масштабирование изображений
- GLU (служебная программа OpenGL), масштабирование изображений
- Служебная программа OpenGL (GLU), автоматический функции текстурирования
- GLU (служебная программа OpenGL), автоматический функции текстурирования
- Служебная программа OpenGL (GLU), изображения текстур
- GLU (служебная программа OpenGL), изображения текстур
- Библиотека GLU, изображения текстур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329507"
---
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="d43a7-110">Обработка изображений для использования в текстурировании</span><span class="sxs-lookup"><span data-stu-id="d43a7-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="d43a7-111">Библиотека служебной программы OpenGL (GLU) обеспечивает масштабирование изображений и автоматическое выполнение функций функции текстурирования для упрощения спецификации изображений текстур.</span><span class="sxs-lookup"><span data-stu-id="d43a7-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="d43a7-112">Функция [**глускалеимаже**](gluscaleimage.md) масштабирует указанное изображение до допустимого размера текстуры; полученный образ можно передать в OpenGL в виде текстуры.</span><span class="sxs-lookup"><span data-stu-id="d43a7-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="d43a7-113">Автоматические функции функции текстурирования, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) и [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), создают изображения текстуры мипмаппед из указанного изображения и передают их в [**glTexImage1D**](glteximage1d.md) и [**glTexImage2D**](glteximage2d.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="d43a7-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 





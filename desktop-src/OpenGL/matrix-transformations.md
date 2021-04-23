---
title: Преобразования матрицы
description: Вершины и нормали преобразуются в матрицы моделвиев и проекции, прежде чем они будут использованы для создания изображения в буфера кадров.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Конвейер обработки OpenGL, матрицы
- матрицы OpenGL
- Матрица моделвиев
- матрица проекции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253173"
---
# <a name="matrix-transformations"></a><span data-ttu-id="5bb03-107">Преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="5bb03-107">Matrix Transformations</span></span>

<span data-ttu-id="5bb03-108">Вершины и нормали преобразуются в матрицы моделвиев и проекции, прежде чем они будут использованы для создания изображения в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="5bb03-108">Vertices and normals are transformed by the modelview and projection matrices before they're used to produce an image in the framebuffer.</span></span> <span data-ttu-id="5bb03-109">Для составления нужных преобразований используйте такие функции, как [**глматриксмоде**](glmatrixmode.md), [**глмултматрикс \***](glmultmatrix.md), [**\* глротате**](glrotate.md), [**\* глтранслате**](gltranslate.md)и [**глскале \***](glscale.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb03-109">Use functions such as [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix\***](glmultmatrix.md), [**glRotate\***](glrotate.md), [**glTranslate\***](gltranslate.md), and [**glScale\***](glscale.md) to compose the desired transformations.</span></span> <span data-ttu-id="5bb03-110">Или непосредственно указать матрицы с [**помощью \* Гллоадматрикс**](glloadmatrix.md) и [**гллоадидентити**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="5bb03-110">Or specify matrices directly with [**glLoadMatrix\***](glloadmatrix.md) and [**glLoadIdentity**](glloadidentity.md).</span></span> <span data-ttu-id="5bb03-111">Используйте [**глпушматрикс**](glpushmatrix.md) и [**глпопматрикс**](glpopmatrix.md) для сохранения и восстановления матриц моделвиев и проекции в соответствующих стеках.</span><span class="sxs-lookup"><span data-stu-id="5bb03-111">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore modelview and projection matrices on their respective stacks.</span></span>

 

 





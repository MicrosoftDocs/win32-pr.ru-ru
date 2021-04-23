---
title: Преобразование координат
description: Библиотека служебной программы OpenGL (GLU) предоставляет несколько часто используемых функций преобразования матрицы.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Служебная программа OpenGL (GLU), функции преобразования матрицы
- GLU (служебная программа OpenGL), функции преобразования матрицы
- функции преобразования матрицы OpenGL
- Служебная программа OpenGL (GLU), преобразование координат
- GLU (служебная программа OpenGL), преобразование координат
- Преобразование координат OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779472"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="e7717-109">Преобразование координат</span><span class="sxs-lookup"><span data-stu-id="e7717-109">Transforming Coordinates</span></span>

<span data-ttu-id="e7717-110">Библиотека служебной программы OpenGL (GLU) предоставляет несколько часто используемых функций преобразования матрицы.</span><span class="sxs-lookup"><span data-stu-id="e7717-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="e7717-111">Вы можете настроить двухмерную ортогональную область просмотра с помощью [**gluOrtho2D**](gluortho2d.md), стандартного вида перспективного представления с использованием [**глуперспективе**](gluperspective.md)или тома представления, центрированного по указанному эйепоинт с [**глулукат**](glulookat.md).</span><span class="sxs-lookup"><span data-stu-id="e7717-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="e7717-112">Каждая из этих функций создает нужную матрицу и применяет ее к текущей матрице с помощью [**глмултматрикс**](glmultmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e7717-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="e7717-113">Функция [**глупиккматрикс**](glupickmatrix.md) упрощает выбор матрицы подбора путем создания матрицы, которая будет ограничивать Рисование небольшой областью окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="e7717-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="e7717-114">При повторном отображении сцены в режиме выделения после применения этой матрицы будут выбраны все объекты, которые будут отображаться рядом с курсором, а сведения о них будут храниться в буфере выбора.</span><span class="sxs-lookup"><span data-stu-id="e7717-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="e7717-115">Дополнительные сведения о режиме выбора см. в разделе "выполнение выбора и обратной связи" для [выбора и обратной связи](performing-selection-and-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="e7717-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="e7717-116">Чтобы определить, где в окне отображается объект, используйте [**глупрожект**](gluproject.md), который преобразует заданные координаты координат *обжкс*, *обжи* и *обжз* в координаты окна с помощью *моделматрикс*, *прожматрикс* и *окна просмотра*.</span><span class="sxs-lookup"><span data-stu-id="e7717-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="e7717-117">Результат сохраняется в *Винкс*, *Вини* и *Винз*.</span><span class="sxs-lookup"><span data-stu-id="e7717-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="e7717-118">Если функция выполнена удачно, возвращается значение GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="e7717-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="e7717-119">Если функция завершается ошибкой, возвращается значение GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="e7717-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="e7717-120">Функция [**глуунпрожект**](gluunproject.md) выполняет обратное преобразование: оно Преобразует указанное окно координат *Винкс*, *Вини* и *Винз* в объектные координаты с помощью *моделматрикс*, *прожматрикс* и *окна просмотра*.</span><span class="sxs-lookup"><span data-stu-id="e7717-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="e7717-121">Результат сохраняется в *обжкс*, *обжи* и *обжз*.</span><span class="sxs-lookup"><span data-stu-id="e7717-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="e7717-122">Если функция выполнена удачно, возвращается значение GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="e7717-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="e7717-123">Если функция завершается ошибкой, возвращается значение GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="e7717-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 





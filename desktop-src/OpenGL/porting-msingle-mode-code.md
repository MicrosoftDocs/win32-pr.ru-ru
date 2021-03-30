---
title: Перенос кода режима МСИНГЛЕ
description: OpenGL не имеет эквивалента для режима МСИНГЛЕ, односекционный режим.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Перенос GL в ГК, режим МСИНГЛЕ
- Перенос из IRI GL, режим МСИНГЛЕ
- перенос в OpenGL из IRI GL, режим МСИНГЛЕ
- Перенос по стандарту OpenGL из IRI GL, режим МСИНГЛЕ
- Режим МСИНГЛЕ
- Перенос GL в ГК, режим одиночной матрицы
- Перенос из IRI GL в одноматричный режим
- перенос в OpenGL из IRI GL, односекционный режим
- Перенос по стандарту OpenGL из IRI GL, односекционный режим
- режим одиночной матрицы
- режим двойной матрицы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411127"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="ce47a-114">Перенос кода режима МСИНГЛЕ</span><span class="sxs-lookup"><span data-stu-id="ce47a-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="ce47a-115">OpenGL не имеет эквивалента для режима **мсингле**, односекционный режим.</span><span class="sxs-lookup"><span data-stu-id="ce47a-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="ce47a-116">Хотя использовать этот режим не рекомендуется, он используется по умолчанию для IRI GL.</span><span class="sxs-lookup"><span data-stu-id="ce47a-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="ce47a-117">Если программа IRI GL использует одноматричный режим, необходимо переписать ее, чтобы использовать только режим двойной матрицы.</span><span class="sxs-lookup"><span data-stu-id="ce47a-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="ce47a-118">OpenGL всегда находится в режиме двойной матрицы и изначально находится в режиме GL \_ моделвиев.</span><span class="sxs-lookup"><span data-stu-id="ce47a-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="ce47a-119">В большинстве случаев код GL ГК в режиме МСИНГЛЕ выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ce47a-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="ce47a-120">где *прожектионматрикс* — одно из следующих: **Орсо**, **ortho2**, **Перспектива** или **Window**.</span><span class="sxs-lookup"><span data-stu-id="ce47a-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="ce47a-121">Чтобы перенести в OpenGL, замените функцию *Прожектионматрикс* **мсингле** -Mode на:</span><span class="sxs-lookup"><span data-stu-id="ce47a-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 





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
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132393"
---
# <a name="porting-msingle-mode-code"></a>Перенос кода режима МСИНГЛЕ

OpenGL не имеет эквивалента для режима **мсингле**, односекционный режим. Хотя использовать этот режим не рекомендуется, он используется по умолчанию для IRI GL. Если программа IRI GL использует одноматричный режим, необходимо переписать ее, чтобы использовать только режим двойной матрицы. OpenGL всегда находится в режиме двойной матрицы и изначально находится в режиме GL \_ моделвиев.

В большинстве случаев код GL ГК в режиме МСИНГЛЕ выглядит следующим образом:

``` syntax
projectionmatrix();
```

где *прожектионматрикс* — одно из следующих: **Орсо**, **ortho2**, **Перспектива** или **Window**. Чтобы перенести в OpenGL, замените функцию *Прожектионматрикс* **мсингле** -Mode на:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 





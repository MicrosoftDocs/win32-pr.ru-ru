---
title: Расширенный Поворот
description: В этом разделе объясняется, как повернуть объект в зависимости от того, где пользователь выполняет манипуляции с вращением.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Касание Windows, поворот
- Касание Windows, Расширенный Поворот
- Касание Windows, манипуляции
- манипуляции, вращение
- манипуляции, Расширенный Поворот
- вращение, дополнительно
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986193"
---
# <a name="advanced-rotation"></a>Расширенный Поворот

В этом разделе объясняется, как повернуть объект в зависимости от того, где пользователь выполняет манипуляции с вращением.

На следующем рисунке показаны два разных способа вращения объекта.

![Иллюстрация, демонстрирующая два типа поворота одного пальца: вокруг центра или вокруг края, с границей, включающей вращение и перевод](images/rotation.png)

В примере а объект обрабатывается вокруг центральной точки объекта. В примере б объект поворачивается вокруг центральной точки манипуляции. Для поддержки манипуляций с точкой, отличной от центральной точки объекта, необходимо выполнить составную манипуляцию, которая выполняет поворот и перевод. В следующем коде показано, как выполняется и вычисляется эта манипуляция.


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Расширенные манипуляции](advanced-manipulations.md)
</dt> <dt>

[Манипуляции](getting-started-with-manipulations.md)
</dt> </dl>

 

 





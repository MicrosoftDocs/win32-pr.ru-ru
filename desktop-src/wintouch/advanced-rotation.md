---
title: Расширенный Поворот
description: В этом разделе объясняется, как повернуть объект в зависимости от того, где пользователь выполняет манипуляции с вращением.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Сенсорный ввод, поворот
- Windows Сенсорный ввод, Расширенный Поворот
- Windows Сенсорный ввод, манипуляции
- манипуляции, вращение
- манипуляции, Расширенный Поворот
- вращение, дополнительно
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dda17ae8076061f7b5b7b935afb2b7f8e5fb10cb270280f7edbb8c23aa896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199520"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Расширенные манипуляции](advanced-manipulations.md)
</dt> <dt>

[Манипуляции](getting-started-with-manipulations.md)
</dt> </dl>

 

 





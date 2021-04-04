---
title: P (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parameters
- подразделение перспективы
- пиксели
- точки
- многоугольники
- Primitives
- матрицы проекции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103988112"
---
# <a name="p-opengl"></a>P (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р.](h.md) [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**параметр**
</dt> <dd>

Значение, передаваемое в качестве аргумента команде OpenGL. Иногда одно из значений, передаваемых по ссылке на команду OpenGL.

</dd> <dt>

<span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**подразделение перспективы**
</dt> <dd>

Деление x, y и z на w выполняется в координатах обрезки. См. также [координаты клипов](c.md).

</dd> <dt>

<span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**растров**
</dt> <dd>

Элемент Picture. Биты в расположении (x, y) всех битпланес в буфера кадров составляют один пиксель (x, y). В изображении в памяти клиента пиксель — это одна группа элементов. В координатах окна OpenGL каждый пиксель соответствует области экрана 1,0 x 1.0. Координаты левого нижнего угла в именах пикселей x, y — (x, y), а правый верхний угол — (x + 1, y + 1).

</dd> <dt>

<span id="opengl_point"></span><span id="OPENGL_POINT"></span>**точки**
</dt> <dd>

Точное расположение в пространстве, которое подготавливается к просмотру как точка конечного диаметра.

</dd> <dt>

<span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**фигуры**
</dt> <dd>

Близкое к краю поверхность, ограниченная краями, заданным вершинами. Каждый треугольник сетки треугольника — это многоугольник, как и каждый грани четырехсторонней сетки грани четырехсторонней. Прямоугольник, заданный параметром Глрект, также является многоугольником.

</dd> <dt>

<span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**простого**
</dt> <dd>

Фигура (точка, линия, многоугольник, точечный рисунок или изображение), которую можно изобразить, сохранять и манипулировать как дискретными сущностями; элементы, из которых создаются крупные графические модели.

</dd> <dt>

<span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**матрица проекции**
</dt> <dd>

Матрица 4x4, которая преобразует точки, линии, многоугольники и растровые позиции из координат глаз в координаты отсечения.

</dd> </dl>

 

 





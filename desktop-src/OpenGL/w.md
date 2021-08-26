---
title: W (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- Windows
- с выровняйтем окон
- координаты окна
- каркасной модели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab63248917d4490d6b577ac490ef6185e173e8b78031a055625e246c17e5485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887834"
---
# <a name="w-opengl"></a>W (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) [](i.md) . [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**окно**
</dt> <dd>

Подобласть буфера кадров, обычно прямоугольная, у которой все пиксели имеют одинаковую конфигурацию буфера. Контекст OpenGL подготавливается к просмотру по одному окну за раз.

</dd> <dt>

<span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**с выровняйтем окон**
</dt> <dd>

При ссылке на сегменты линии или границы многоугольника подразумевает, что они являются параллельными границами окна. (В OpenGL окно прямоугольное, с горизонтальными и вертикальными краями). При ссылке на шаблон многоугольника подразумевает, что шаблон фиксирован относительно исходного окна.

</dd> <dt>

<span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**координаты окна**
</dt> <dd>

Система координат окна. Важно различать имена пикселей, которые являются дискретными, и систему координат окна, которая является непрерывной. Например, пиксель в левом нижнем углу окна — пиксель (0, 0); координаты окна центра этого пикселя: (0,5, 0,5, z). Обратите внимание, что координаты окон включают глубину, z, компонент и то, что этот компонент также является непрерывным.

</dd> <dt>

<span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**каркасной модели**
</dt> <dd>

Представление объекта, содержащего только сегменты линий. Как правило, сегменты линии обозначают границы многоугольников.

</dd> </dl>

 

 





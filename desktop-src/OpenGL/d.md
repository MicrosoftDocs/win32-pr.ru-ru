---
title: D (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- cueing глубины
- списки вывода
- сглаживания
- двойная буферизация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebc4d797371a966020fbdaff3d62d845ecbbfdc5f21f6e37393e01b2defad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554624"
---
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Длина**
</dt> <dd>

Обычно относится к координатам окна z.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**cueing глубины**
</dt> <dd>

Метод подготовки к просмотру, который назначает цвет на основе расстояния от точки зрения.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**список отображаемых**
</dt> <dd>

Именованный список команд OpenGL. Списки дисплеев всегда хранятся на сервере, поэтому списки для уменьшения сетевого трафика в средах клиента и сервера можно использовать. Содержимое списка отображений может быть предварительно обработано, поэтому оно может выполняться более эффективно, чем тот же набор команд OpenGL, который выполняется в режиме интерпретации. Такая предварительная обработка особенно важна для ресурсоемких команд, таких как [**глтексимаже**](glteximage1d.md).

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**сглаживания**
</dt> <dd>

Метод для увеличения воспринимаемого диапазона цветов в изображении за счет использования пространственного разрешения. Смежным пикселам присваиваются разные значения цвета. При просмотре с расстояния эти цвета по-видимому смешиваются с одним промежуточным цветом. Эта методика похожа на половину Тонинг, используемую в публикациях черно-белых, для получения оттенков серого.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**Двойная буферизация**
</dt> <dd>

Использование контекстов OpenGL, в которых буферы фона и фона имеют двойную буферизацию. Гладкая анимация достигается за счет отрисовки только заднего буфера (который не отображается), что приводит к замене передних и задних буферов.

</dd> </dl>

 

 





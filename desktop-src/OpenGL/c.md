---
title: C (OpenGL)
description: Определения терминов OpenGL, которые начинаются с буквы C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- клиентские компьютеры
- память клиента
- Координаты клипа
- усечение
- цветовой индекс
- режим индексирования цветов
- цветовые карты
- components
- контексты
- выпуклой
- выпуклая оболочка
- система координат
- установлена
- текущая матрица
- Текущая растровая размещается
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071016"
---
# <a name="c-opengl"></a><span data-ttu-id="7fa22-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="7fa22-118">C (OpenGL)</span></span>

<span data-ttu-id="7fa22-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [р](h.md) . [](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="7fa22-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="7fa22-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**клиентский компьютер**</span><span class="sxs-lookup"><span data-stu-id="7fa22-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-121">Компьютер, с которого выдаются команды OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7fa22-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="7fa22-122">Компьютер, который выдает команды OpenGL, может быть подключен по сети к другому компьютеру, на котором выполняются команды, или на одном и том же компьютере могут выдаваться и выполняться команды.</span><span class="sxs-lookup"><span data-stu-id="7fa22-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="7fa22-123">См. также [Server](s.md).</span><span class="sxs-lookup"><span data-stu-id="7fa22-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**память клиента**</span><span class="sxs-lookup"><span data-stu-id="7fa22-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-125">Основной объем памяти (в которой хранятся переменные программы) клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="7fa22-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**Координаты клипа**</span><span class="sxs-lookup"><span data-stu-id="7fa22-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-127">Система координат, которая соответствует преобразованию матрицы проекции и предшествует подразделению перспективы.</span><span class="sxs-lookup"><span data-stu-id="7fa22-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="7fa22-128">Представление — обрезка тома выполняется в координатах клипов, но отсечение с конкретным приложением не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fa22-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="7fa22-129">См. также [обрезание, зависящее от приложения](a.md).</span><span class="sxs-lookup"><span data-stu-id="7fa22-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**вырезая**</span><span class="sxs-lookup"><span data-stu-id="7fa22-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-131">Исключение части геометрического примитива, находящегося за пределами половины пространства, определенного плоскостью обрезки.</span><span class="sxs-lookup"><span data-stu-id="7fa22-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="7fa22-132">Точки просто отклоняются, если они выходят за пределы.</span><span class="sxs-lookup"><span data-stu-id="7fa22-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="7fa22-133">Часть строки или многоугольника, находящегося за пределами половины пространства, исключается, и при необходимости создаются дополнительные вершины для завершения примитива в пределах обрезки.</span><span class="sxs-lookup"><span data-stu-id="7fa22-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="7fa22-134">Геометрические примитивы и текущая позиция в виде растровой позиции (если они заданы) всегда обрезаются по шести половинных пробелам, определенным левым, правым, нижним, верхним, близким и дальнеимися плоскостями отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="7fa22-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="7fa22-135">Приложения могут указывать дополнительные отрезкиные плоскости для конкретного приложения, которые применяются в координатах глаз.</span><span class="sxs-lookup"><span data-stu-id="7fa22-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**цветовой индекс**</span><span class="sxs-lookup"><span data-stu-id="7fa22-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-137">Одно значение, представляющее цвет по имени, а не по значению.</span><span class="sxs-lookup"><span data-stu-id="7fa22-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="7fa22-138">Цветовые индексы OpenGL обрабатываются как непрерывные значения (например, числа с плавающей запятой), а такие операции, как интерполяция и дизеринг, выполняются на них.</span><span class="sxs-lookup"><span data-stu-id="7fa22-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="7fa22-139">Цветовые индексы, хранящиеся в буфере фрейма, всегда имеют целочисленные значения.</span><span class="sxs-lookup"><span data-stu-id="7fa22-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="7fa22-140">Индексы с плавающей запятой преобразуются в целые числа путем округления до ближайшего целого значения.</span><span class="sxs-lookup"><span data-stu-id="7fa22-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**режим индексирования цветов**</span><span class="sxs-lookup"><span data-stu-id="7fa22-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-142">Режим контекста OpenGL, в котором буферы цветов хранят цветовые индексы, а не красные, зеленые, синие и альфа-компоненты цвета.</span><span class="sxs-lookup"><span data-stu-id="7fa22-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**Цветовая схема**</span><span class="sxs-lookup"><span data-stu-id="7fa22-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-144">Таблица сопоставлений "индекс-RGB", доступ к которым осуществляется аппаратным обеспечением экрана.</span><span class="sxs-lookup"><span data-stu-id="7fa22-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="7fa22-145">Каждый цветовой индекс считывается из буфера цвета, преобразуется в RGB, тройным путем поиска в цветовой карте, и отправляется монитору.</span><span class="sxs-lookup"><span data-stu-id="7fa22-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**см**</span><span class="sxs-lookup"><span data-stu-id="7fa22-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-147">Единичное, непрерывное (например, с плавающей запятой) значение, представляющее интенсивность или количество.</span><span class="sxs-lookup"><span data-stu-id="7fa22-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="7fa22-148">Обычно значение компонента, равное нулю, представляет собой минимальное значение или интенсивность, а значение компонента, равное единице, представляет максимальное значение или интенсивность, хотя иногда используются другие нормализации.</span><span class="sxs-lookup"><span data-stu-id="7fa22-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="7fa22-149">Поскольку значения компонентов интерпретируется в нормализованном диапазоне, они задаются независимо от фактического разрешения.</span><span class="sxs-lookup"><span data-stu-id="7fa22-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="7fa22-150">Например, RGB Triple (1, 1, 1) является белым, независимо от того, хранят ли буферы цветов 4, 8 или 12 бит.</span><span class="sxs-lookup"><span data-stu-id="7fa22-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="7fa22-151">Компоненты, которые выходят за пределы диапазона, обычно преобразуются в нормализованный диапазон, а не усекаются или не обрабатываются иным образом.</span><span class="sxs-lookup"><span data-stu-id="7fa22-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="7fa22-152">Например, RGB Triple (1,4, 1,5, 0,9) замещается в (1,0, 1,0, 0,9) перед тем, как он будет использоваться для обновления буфера цвета.</span><span class="sxs-lookup"><span data-stu-id="7fa22-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="7fa22-153">Красный, зеленый, синий, альфа и глубина всегда обрабатываются как компоненты, а не как индексы.</span><span class="sxs-lookup"><span data-stu-id="7fa22-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**локального**</span><span class="sxs-lookup"><span data-stu-id="7fa22-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-155">Полный набор переменных состояния OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7fa22-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="7fa22-156">Обратите внимание, что содержимое буфера кадров не входит в состояние OpenGL, но конфигурация буфера кадров имеет значение.</span><span class="sxs-lookup"><span data-stu-id="7fa22-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**выпуклой**</span><span class="sxs-lookup"><span data-stu-id="7fa22-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-158">Условие многоугольника, в котором никакая прямая линия в плоскости многоугольника пересекает многоугольник больше двух.</span><span class="sxs-lookup"><span data-stu-id="7fa22-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**выпуклой поверхности**</span><span class="sxs-lookup"><span data-stu-id="7fa22-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-160">Наименьший регион выпуклой, включающий в себя указанную группу точек.</span><span class="sxs-lookup"><span data-stu-id="7fa22-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="7fa22-161">В двух измерениях выпуклой поверхности, по сути, растягивает резиновую полоску вокруг точек, чтобы все точки находились в пределах диапазона.</span><span class="sxs-lookup"><span data-stu-id="7fa22-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**система координат**</span><span class="sxs-lookup"><span data-stu-id="7fa22-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-163">В n-мерном пространстве набор n линейно независимых векторов, исходящих из одной точки (которая называется точкой отсчета).</span><span class="sxs-lookup"><span data-stu-id="7fa22-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="7fa22-164">Группа координат задает точку в n-мерном пространстве, набор n независимых векторов, привязанных к точке (называемой происхождением).</span><span class="sxs-lookup"><span data-stu-id="7fa22-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="7fa22-165">Набор координат задает точку в пространстве (или вектор с началом в точке отсчета), указывая расстояние, которое нужно преодолеть в направлении каждого вектора, чтобы добраться в эту точку (или в конец вектора).</span><span class="sxs-lookup"><span data-stu-id="7fa22-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="7fa22-166">(или вектор из источника), указывая, насколько далеко вдоль каждого вектора достигается точка (или кончик вектора).</span><span class="sxs-lookup"><span data-stu-id="7fa22-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**установлена**</span><span class="sxs-lookup"><span data-stu-id="7fa22-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-168">Процесс удаления лицевой или задней стороны многоугольника, чтобы изображение не нарисовано.</span><span class="sxs-lookup"><span data-stu-id="7fa22-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**текущая матрица**</span><span class="sxs-lookup"><span data-stu-id="7fa22-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-170">Матрица, которая преобразует координаты в одной системе координат в координаты другой системы.</span><span class="sxs-lookup"><span data-stu-id="7fa22-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="7fa22-171">В OpenGL есть три текущие матрицы: матрица моделвиев, которая преобразует координаты объектов (координаты, заданные программистом) в координаты глаз; Матрица перспективы, которая преобразует координаты глаза в координаты отсечения; и матрица текстур, которая преобразует указанные или созданные координаты текстуры, как описано в матрице.</span><span class="sxs-lookup"><span data-stu-id="7fa22-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="7fa22-172">Каждая текущая матрица является верхним элементом в стеке матриц.</span><span class="sxs-lookup"><span data-stu-id="7fa22-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="7fa22-173">Каждому из трех стеков можно управлять с помощью команд управления матрицами OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7fa22-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="7fa22-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**Текущая растровая размещается**</span><span class="sxs-lookup"><span data-stu-id="7fa22-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="7fa22-175">Координата окна, указывающая положение примитива изображения при его растрировании.</span><span class="sxs-lookup"><span data-stu-id="7fa22-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="7fa22-176">Текущая растровая размещается и другие текущие параметры растрового изображения обновляются при вызове Глрастерпос.</span><span class="sxs-lookup"><span data-stu-id="7fa22-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 





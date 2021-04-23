---
title: Глоссарий DirectComposition
description: В этом разделе определяются термины Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338049"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="ec138-103">Глоссарий DirectComposition</span><span class="sxs-lookup"><span data-stu-id="ec138-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="ec138-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="ec138-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="ec138-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="ec138-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="ec138-106">В этом разделе определяются термины Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="ec138-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="ec138-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**Функция анимации**</span><span class="sxs-lookup"><span data-stu-id="ec138-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-108">Конструкция, которая указывает, как изменяется значение одного свойства объекта за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="ec138-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**объект Animation**</span><span class="sxs-lookup"><span data-stu-id="ec138-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-110">Объект, представляющий функцию для анимации свойств другого объекта.</span><span class="sxs-lookup"><span data-stu-id="ec138-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**сегмент анимации**</span><span class="sxs-lookup"><span data-stu-id="ec138-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-112">Фундаментальные определения времени функции анимации; Это примитивы, из которых строятся более сложные и более высокие функции анимации.</span><span class="sxs-lookup"><span data-stu-id="ec138-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**задний буфер**</span><span class="sxs-lookup"><span data-stu-id="ec138-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-114">Прямоугольник памяти, в который приложение может непосредственно выполнять запись.</span><span class="sxs-lookup"><span data-stu-id="ec138-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="ec138-115">Задний буфер никогда не отображается на мониторе напрямую.</span><span class="sxs-lookup"><span data-stu-id="ec138-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**разделах**</span><span class="sxs-lookup"><span data-stu-id="ec138-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-117">Группа вызовов метода DirectComposition, которые обрабатываются атомарно.</span><span class="sxs-lookup"><span data-stu-id="ec138-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**массив**</span><span class="sxs-lookup"><span data-stu-id="ec138-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-119">Цветовой буфер с альфа-каналом или без него, который находится в системной или видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="ec138-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**режим границы**</span><span class="sxs-lookup"><span data-stu-id="ec138-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-121">Свойство визуального элемента Microsoft DirectComposition, которое влияет на то, как края растрового изображения обрабатываются при преобразовании растрового изображения таким способом, чтобы границы не совпадали с целыми координатами.</span><span class="sxs-lookup"><span data-stu-id="ec138-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="ec138-122">Он также влияет на то, как содержимое обрезается по углам клипа, имеющего скругленные углы, и на границе зажима, преобразованной таким способом, что границы не вычисляются с помощью целых координат.</span><span class="sxs-lookup"><span data-stu-id="ec138-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**Объект Clip**</span><span class="sxs-lookup"><span data-stu-id="ec138-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-124">Объект, представляющий прямоугольник обрезки.</span><span class="sxs-lookup"><span data-stu-id="ec138-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**прямоугольник обрезки**</span><span class="sxs-lookup"><span data-stu-id="ec138-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-126">Набор координат, определяющих область содержимого растрового изображения визуального элемента, отображаемого на экране при подготовке к просмотру растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="ec138-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**скрытыми**</span><span class="sxs-lookup"><span data-stu-id="ec138-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-128">Чтобы временно запретить диспетчер окон рабочего стола (DWM) рисовать окно на экране.</span><span class="sxs-lookup"><span data-stu-id="ec138-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="ec138-129">Приложения обычно заменяют окно, тогда как DirectComposition использует растровое изображение окна в композиции.</span><span class="sxs-lookup"><span data-stu-id="ec138-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="ec138-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-131">Для отправки пакета команд в Директкомпоситиондиректкомпоситион для обработки.</span><span class="sxs-lookup"><span data-stu-id="ec138-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**составной режим**</span><span class="sxs-lookup"><span data-stu-id="ec138-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-133">Один из способов смешения двух точечных рисунков (источника и назначения) для достижения определенного результата.</span><span class="sxs-lookup"><span data-stu-id="ec138-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**композиции**</span><span class="sxs-lookup"><span data-stu-id="ec138-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-135">Коллекция точечных рисунков, которые комбинируются и обрабатываются путем применения различных преобразований, эффектов и анимации для создания предполагаемого визуального результата в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="ec138-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**окно цели композиции**</span><span class="sxs-lookup"><span data-stu-id="ec138-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-137">Окно, к которому привязано визуальное дерево, в котором рисуется полученная композиция.</span><span class="sxs-lookup"><span data-stu-id="ec138-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**тень**</span><span class="sxs-lookup"><span data-stu-id="ec138-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-139">Операция, изменяющая растровое изображение визуального дерева, обычно путем применения шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="ec138-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Группа эффектов**</span><span class="sxs-lookup"><span data-stu-id="ec138-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-141">Группа эффектов точечных рисунков, которые применяются вместе для изменения растрирования поддерева визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="ec138-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**NOFRAMES**</span><span class="sxs-lookup"><span data-stu-id="ec138-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-143">Итерация механизма композиции, которая создает растрирование визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="ec138-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**Интерфейсный буфер**</span><span class="sxs-lookup"><span data-stu-id="ec138-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-145">Прямоугольник памяти, который преобразуется графическим адаптером и отображается на мониторе.</span><span class="sxs-lookup"><span data-stu-id="ec138-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**Режим интерполяции**</span><span class="sxs-lookup"><span data-stu-id="ec138-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-147">Свойство, определяющее способ формирования точечного рисунка при преобразовании таким способом, что нет соответствия "один к одному" между пикселями в точечном рисунке и пикселами на экране.</span><span class="sxs-lookup"><span data-stu-id="ec138-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**корневой визуальный элемент**</span><span class="sxs-lookup"><span data-stu-id="ec138-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-149">Визуальный элемент, из которого все остальные визуальные элементы в визуальном дереве отображаются по убыванию.</span><span class="sxs-lookup"><span data-stu-id="ec138-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**цепочка подкачки**</span><span class="sxs-lookup"><span data-stu-id="ec138-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-151">Коллекция из одного или нескольких задних буферов, которые могут быть последовательно представлены в интерфейсном буфере</span><span class="sxs-lookup"><span data-stu-id="ec138-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="ec138-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**подоб**</span><span class="sxs-lookup"><span data-stu-id="ec138-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-153">Представление линейной области отображения памяти, которая обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="ec138-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Преобразует**</span><span class="sxs-lookup"><span data-stu-id="ec138-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-155">Матрица, представляющая преобразование координат в двухмерном или трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="ec138-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Группа преобразований**</span><span class="sxs-lookup"><span data-stu-id="ec138-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-157">Коллекция преобразований, матрица которых умножается в том порядке, в котором они указаны в коллекции перед применением к визуальному элементу.</span><span class="sxs-lookup"><span data-stu-id="ec138-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**внешнего**</span><span class="sxs-lookup"><span data-stu-id="ec138-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-159">Объект, содержащий необязательную ссылку на объект Bitmap, и набор свойств, определяющих место и способ отрисовки растрового изображения на экране.</span><span class="sxs-lookup"><span data-stu-id="ec138-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**визуальный объект**</span><span class="sxs-lookup"><span data-stu-id="ec138-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-161">См. раздел [*Visual*](/windows).</span><span class="sxs-lookup"><span data-stu-id="ec138-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="ec138-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**визуальное поддерево**</span><span class="sxs-lookup"><span data-stu-id="ec138-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-163">Часть визуального дерева, состоящая из конкретного визуального элемента и всех его дочерних элементов и потомков.</span><span class="sxs-lookup"><span data-stu-id="ec138-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**визуальное дерево**</span><span class="sxs-lookup"><span data-stu-id="ec138-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-165">Иерархическая коллекция визуальных элементов, используемых для создания композиции.</span><span class="sxs-lookup"><span data-stu-id="ec138-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="ec138-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**цепочка подкачки без окон**</span><span class="sxs-lookup"><span data-stu-id="ec138-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="ec138-167">Цепочка подкачки, связанная с визуальным объектом DirectComposition, а не окном.</span><span class="sxs-lookup"><span data-stu-id="ec138-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 
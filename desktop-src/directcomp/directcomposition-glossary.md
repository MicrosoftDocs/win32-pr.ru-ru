---
title: Глоссарий DirectComposition
description: В этом разделе определяются термины Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d6a6f39de62339bf5de0ea7b4976fa19f60c4bd2ff549a732acee43d546256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985434"
---
# <a name="directcomposition-glossary"></a>Глоссарий DirectComposition

> [!NOTE]
> для приложений на Windows 10 рекомендуется использовать интерфейсы api Windows. UI. компоновки вместо DirectComposition. Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).

В этом разделе определяются термины Microsoft DirectComposition.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**Функция анимации**
</dt> <dd>

Конструкция, которая указывает, как изменяется значение одного свойства объекта за определенный период времени.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**объект Animation**
</dt> <dd>

Объект, представляющий функцию для анимации свойств другого объекта.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**сегмент анимации**
</dt> <dd>

Фундаментальные определения времени функции анимации; Это примитивы, из которых строятся более сложные и более высокие функции анимации.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**задний буфер**
</dt> <dd>

Прямоугольник памяти, в который приложение может непосредственно выполнять запись. Задний буфер никогда не отображается на мониторе напрямую.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**разделах**
</dt> <dd>

Группа вызовов метода DirectComposition, которые обрабатываются атомарно.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**массив**
</dt> <dd>

Цветовой буфер с альфа-каналом или без него, который находится в системной или видеопамяти.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**режим границы**
</dt> <dd>

Свойство визуального элемента Microsoft DirectComposition, которое влияет на то, как края растрового изображения обрабатываются при преобразовании растрового изображения таким способом, чтобы границы не совпадали с целыми координатами. Он также влияет на то, как содержимое обрезается по углам клипа, имеющего скругленные углы, и на границе зажима, преобразованной таким способом, что границы не вычисляются с помощью целых координат.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**Объект Clip**
</dt> <dd>

Объект, представляющий прямоугольник обрезки.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**прямоугольник обрезки**
</dt> <dd>

Набор координат, определяющих область содержимого растрового изображения визуального элемента, отображаемого на экране при подготовке к просмотру растрового изображения.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**скрытыми**
</dt> <dd>

Чтобы временно запретить диспетчер окон рабочего стола (DWM) рисовать окно на экране. Приложения обычно заменяют окно, тогда как DirectComposition использует растровое изображение окна в композиции.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**Сохраните**
</dt> <dd>

Для отправки пакета команд в Директкомпоситиондиректкомпоситион для обработки.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**составной режим**
</dt> <dd>

Один из способов смешения двух точечных рисунков (источника и назначения) для достижения определенного результата.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**композиции**
</dt> <dd>

Коллекция точечных рисунков, которые комбинируются и обрабатываются путем применения различных преобразований, эффектов и анимации для создания предполагаемого визуального результата в пользовательском интерфейсе приложения.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**окно цели композиции**
</dt> <dd>

Окно, к которому привязано визуальное дерево, в котором рисуется полученная композиция.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**тень**
</dt> <dd>

Операция, изменяющая растровое изображение визуального дерева, обычно путем применения шейдера пикселей.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Группа эффектов**
</dt> <dd>

Группа эффектов точечных рисунков, которые применяются вместе для изменения растрирования поддерева визуального элемента.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**NOFRAMES**
</dt> <dd>

Итерация механизма композиции, которая создает растрирование визуального дерева.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**Интерфейсный буфер**
</dt> <dd>

Прямоугольник памяти, который преобразуется графическим адаптером и отображается на мониторе.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**Режим интерполяции**
</dt> <dd>

Свойство, определяющее способ формирования точечного рисунка при преобразовании таким способом, что нет соответствия "один к одному" между пикселями в точечном рисунке и пикселами на экране.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**корневой визуальный элемент**
</dt> <dd>

Визуальный элемент, из которого все остальные визуальные элементы в визуальном дереве отображаются по убыванию.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**цепочка подкачки**
</dt> <dd>

Коллекция из одного или нескольких задних буферов, которые могут быть последовательно представлены в интерфейсном буфере

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**подоб**
</dt> <dd>

Представление линейной области отображения памяти, которая обычно находится в отображаемой памяти видеокарты, хотя поверхности могут существовать в системной памяти.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Преобразует**
</dt> <dd>

Матрица, представляющая преобразование координат в двухмерном или трехмерном пространстве.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Группа преобразований**
</dt> <dd>

Коллекция преобразований, матрица которых умножается в том порядке, в котором они указаны в коллекции перед применением к визуальному элементу.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**внешнего**
</dt> <dd>

Объект, содержащий необязательную ссылку на объект Bitmap, и набор свойств, определяющих место и способ отрисовки растрового изображения на экране.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**визуальный объект**
</dt> <dd>

См. раздел [*Visual*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**визуальное поддерево**
</dt> <dd>

Часть визуального дерева, состоящая из конкретного визуального элемента и всех его дочерних элементов и потомков.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**визуальное дерево**
</dt> <dd>

Иерархическая коллекция визуальных элементов, используемых для создания композиции.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**цепочка подкачки без окон**
</dt> <dd>

Цепочка подкачки, связанная с визуальным объектом DirectComposition, а не окном.

</dd> </dl>

 

 
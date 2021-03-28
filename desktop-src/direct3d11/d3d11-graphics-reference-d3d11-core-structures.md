---
title: Базовые структуры Direct3D 11
description: В этом разделе содержатся сведения о базовых структурах.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- структуры, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413298"
---
# <a name="direct3d-11-core-structures"></a>Базовые структуры Direct3D 11

В этом разделе содержатся сведения о базовых структурах.

## <a name="in-this-section"></a>В этом разделе

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br/></td>
<td>Описывает состояние смешения, которое используется при вызове метода <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: креатеблендстате</strong></a> для создания объекта состояния смешения. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает состояние смешения, которое используется при вызове метода <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> для создания объекта состояния смешения. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br/></td>
<td>Определяет трехмерное поле.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br/></td>
<td>Описывает счетчик.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br/></td>
<td>Сведения о возможностях счетчика производительности видеоадаптера.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br/></td>
<td>Описывает состояние трафарета глубины.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br/></td>
<td>Операции с наборами элементов, которые могут быть выполнены на основе результатов теста трафарета.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Аргументы для нарисованного непрямого индексированного экземпляра. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Аргументы для рисования с непрямыми экземплярами. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает сведения об архитектуре адаптера Direct3D 11,1.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описание параметров функции Direct3D 9 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br/></td>
<td>Описание параметров функции Direct3D 9 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает поддержку теневой версии Direct3D 9 в текущем графическом драйвере. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br/></td>
<td>Описывает, поддерживается ли простой способ создания экземпляров.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br/></td>
<td>Описывает поддержку шейдера вычислений и необработанных и структурированных буферов в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описание параметров функции Direct3D 11,1 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br/></td>
<td>Описание параметров функции Direct3D 11,2 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br/></td>
<td>Описание параметров функции Direct3D 11,3 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br/></td>
<td>Описание параметров функции Direct3D 11,3 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br/></td>
<td>Описание параметров функции Direct3D 11,4 в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br/></td>
<td>Описывает уровень поддержки общих ресурсов в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br/></td>
<td>Описывает поддержку типов данных Double в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br/></td>
<td>Описывает, какие ресурсы поддерживаются текущим драйвером графики для заданного формата.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Описание неупорядоченных параметров ресурсов, поддерживаемых текущим графическим драйвером для заданного формата.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br/></td>
<td>Описание функций, поддерживаемых виртуальным адресом GPU, включая максимальное число битов на ресурс и на процесс. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br/></td>
<td>Описывает, поддерживается ли метод профилирования GPU.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br/></td>
<td>Описывает уровень кэширования шейдера, поддерживаемый в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает варианты поддержки точности для шейдеров в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br/></td>
<td>Описывает функции многопоточности, поддерживаемые текущим драйвером графики.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br/></td>
<td>Описание одного элемента для этапа входного ассемблера.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br/></td>
<td>Запрос сведений о графических-конвейерных действиях между вызовами <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ссылку ID3D11DeviceContext:: Begin</strong></a> и <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ссылку ID3D11DeviceContext:: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br/></td>
<td>Запрос сведений о количестве потоковых данных, помещенных в поток потока вывода между <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ссылку ID3D11DeviceContext:: Begin</strong></a> и <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ссылку ID3D11DeviceContext:: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br/></td>
<td>Запрос сведений о надежности запроса метки времени.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br/></td>
<td>Описывает запрос.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br/></td>
<td>Описывает запрос.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br/></td>
<td>Описывает состояние средства отображения программной прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает состояние средства отображения программной прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br/></td>
<td>Описывает состояние средства отображения программной прорисовки.<br/></td>
</tr>
<tr>
<td><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br/></td>
<td>D3D11_RECT объявляется следующим образом:<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br/></td>
<td>Описывает состояние смешения для целевого объекта прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Эта структура поддерживается средой выполнения Direct3D 11,1, которая доступна в операционных системах Windows 8 и более поздних версий.
</blockquote>
<br/> Описывает состояние смешения для целевого объекта прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br/></td>
<td>Описывает состояние образца.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br/></td>
<td>Описание элемента вершины в буфере вершин в выходном слоте.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br/></td>
<td>Определяет размеры окна просмотра.<br/></td>
</tr>
</tbody>
</table>

Кроме того, в D3D11. h определена структура 2D Rectangle.

```cpp
typedef RECT D3D11_RECT;
```

Документацию см. в разделе [Rect](/previous-versions/dd162897%28v%3dvs.85%29) в [Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>См. также

[Справочник по основным](d3d11-graphics-reference-d3d11-core.md)
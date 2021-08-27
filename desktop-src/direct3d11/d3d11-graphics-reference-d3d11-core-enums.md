---
title: Базовые перечисления Direct3D 11
description: В этом разделе содержатся сведения о базовых перечислениях.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- перечисления, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0daf03ca2114f67935e1eb89f34b31306e31fc0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623120"
---
# <a name="direct3d-11-core-enumerations"></a>Базовые перечисления Direct3D 11

В этом разделе содержатся сведения о базовых перечислениях.

## <a name="in-this-section"></a>В этом разделе

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a><br/></td>
<td>Необязательные флаги, управляющие поведением <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ссылку ID3D11DeviceContext:: GetData</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a><br/></td>
<td>Коэффициенты смешения, которые модуляции значений для шейдера пикселей и целевого объекта прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a><br/></td>
<td>Операция смешения RGB или Alpha.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a><br/></td>
<td>Указывает части трафарета глубины, которые необходимо очистить. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a><br/></td>
<td>Определение того, какие компоненты каждого пикселя целевого объекта отрисовки доступны для записи во время смешения.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a><br/></td>
<td>Параметры сравнения.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a><br/></td>
<td>Определяет, включено ли консервативное растрирование.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a><br/></td>
<td>Указывает, поддерживает ли оборудование и драйверы консервативную растрирование и уровень уровня.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a><br/></td>
<td>Задает контекст, в котором происходит запрос.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в Windows 8 и более поздних операционных системах.
</blockquote>
<br/> Указывает способ обработки существующего содержимого ресурса во время операции копирования или обновления региона в этом ресурсе.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a><br/></td>
<td>Параметры счетчиков производительности.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a><br/></td>
<td>Тип данных счетчика производительности.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a><br/></td>
<td>Описывает параметры, используемые для создания устройства.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a><br/></td>
<td>Описывает флаги, используемые для создания объекта состояния контекста устройства (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) с помощью метода <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1:: креатедевицеконтекстстате</strong></a> .<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a><br/></td>
<td>Показывает, что треугольники, направленные в определенное направление, не рисуются.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a><br/></td>
<td>Определяет часть буфера шаблона глубины для записи данных глубины.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a><br/></td>
<td>Параметры контекста устройства.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a><br/></td>
<td>Параметры функции Direct3D 11.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a><br/></td>
<td>Задает параметры ограждения. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a><br/></td>
<td>Определяет режим заполнения, используемый при отрисовке треугольников.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a><br/></td>
<td>Параметры фильтрации во время выборки текстуры.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a><br/></td>
<td>Типы фильтров "увеличение" или "минификации".<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a><br/></td>
<td>Указывает тип сокращения фильтра образцов. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a><br/></td>
<td>Какие ресурсы поддерживаются для заданного формата и устройства (см. раздел <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device:: чеккформатсуппорт</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: чеккфеатуресуппорт</strong></a>).<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Варианты поддержки неупорядоченных ресурсов для ресурса шейдера вычислений (см. <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: чеккфеатуресуппорт</strong></a>). <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a><br/></td>
<td>Тип данных, содержащихся во входном слоте.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в Windows 8 и более поздних операционных системах.
</blockquote>
<br/> Указывает логические операции, которые необходимо настроить для целевого объекта прорисовки.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a><br/></td>
<td>Указывает, как конвейер интерпретирует геометрические или поверхностиные примитивы ввода шейдера. <br/></td>
</tr>
<tr>
<td><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a><br/></td>
<td>Способ, с помощью которого конвейер интерпретирует данные вершин, привязанные к этапу ассемблера ввода. Эти значения примитивной топологии определяют, как данные вершин подготавливаются к просмотру на экране.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a><br/></td>
<td>Типы запросов.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a><br/></td>
<td>Флаги, описывающие поведение других запросов.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a><br/></td>
<td>Параметры для возведения ошибки в непродолжаемое исключение.<br/></td>
</tr>
<tr>
<td><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a><br/></td>
<td>Описывает уровень поддержки кэширования шейдеров в текущем графическом драйвере.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
это перечисление поддерживается средой выполнения Direct3D 11,1, которая доступна в Windows 8 и более поздних операционных системах.
</blockquote>
<br/> Значения, задающих минимальные уровни точности на стадиях шейдера.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a><br/></td>
<td>Определяет константы, указывающие уровень поддержки общих ресурсов.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a><br/></td>
<td>Операции с наборами элементов, которые могут быть выполнены во время тестирования шаблона глубины.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a><br/></td>
<td>Определение способа разрешения координат текстуры, которые выходят за пределы границ текстуры.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a><br/></td>
<td>Различные грани текстуры Куба.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a><br/></td>
<td>Указывает уровень уровня, на котором поддерживаются мозаичные ресурсы.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Связанные темы

[Справочник по коду](d3d11-graphics-reference-d3d11-core.md)

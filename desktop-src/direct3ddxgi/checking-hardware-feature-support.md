---
description: В этом разделе описывается, как проверить поддержку формата для оборудования на уровне функций Direct3D с помощью вызовов API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 'Проверка поддержки компонентов оборудования '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ee68a97b30c9828e2a5d27aadb58d668b74858
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624070"
---
# <a name="checking-hardware-feature-support"></a>Проверка поддержки компонентов оборудования 

В этом разделе описывается, как проверить поддержку формата для оборудования на уровне функций Direct3D с помощью вызовов API.

Для D3D11 используйте [**ID3D11Device:: чеккформатсуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) для программной проверки сведений в предыдущих разделах. Для D3D12 используйте [**ID3D12:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Формат целевого объекта</th>
<th>D3D12</th>
<th>D3D11</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Буфер</td>
<td>D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Буфер вершин входного ассемблера</td>
<td>D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Буфер входного индекса ассемблера</td>
<td>D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Потоковый буфер вывода</td>
<td>D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Texture1D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>TextureCube</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Шейдер LD</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Пример шейдера (любой фильтр)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Sample_c шейдера (фильтр сравнения)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Пример шейдера (Mono 1_bit_filter)</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Gather4 шейдера</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Gather4_c шейдера</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Mipmap</td>
<td>D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Автоматическое создание mipmap</td>
<td><blockquote>
[!Note]<br />
D3D12 больше не имеет выделенных функций создания mipmap. Приложения должны реализовывать его самостоятельно с помощью шейдеров.
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>рендертаржет</td>
<td>D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Рендертаржет для наложения</td>
<td>D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Выходная операция логики слияния</td>
<td>D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</td>
<td>D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Целевой объект глубины или трафарета</td>
<td>D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Необработанные UAV и SRV</td>


</tr>
<tr class="even">
<td>Структурированные UAV и SRV</td>


</tr>
<tr class="odd">
<td>Типизированный UAV</td>
<td>D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV типизированное хранилище</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>Типизированная Загрузка UAV</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV атомарное Добавление</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>UAV атомарные побитовые операции</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV атомарный CMP&Store/CMP&</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>UAV Atomic Exchange</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>UAV Atomic со знаком min/max</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="odd">
<td>UAV Atomic неподписанные min/max</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Блокируемый ЦП</td>
<td><blockquote>
[!Note]<br />
Только один формат исключает доступ к ЦП (420_OPAQUE).
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>многопримерная Рендертаржет</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>8X многопримерный Рендертаржет</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Другое число с выборке</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Многопримерное разрешение</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Многовыборочная Загрузка</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Отображение Scan-Out</td>
<td>D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Приведение в битовой структуре</td>
<td>D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Поддержка видеодекодера</td>
<td>D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Вход обработчика видео</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="even">
<td>Выходные данные обработчика видео</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Общий ресурс</td>
<td><blockquote>
[!Note]<br />
Текстуры всех форматов могут быть общими зафиксированными ресурсами или помещены в общие кучи.
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Переводимая в качестве буфера ввода полная типизация</td>
<td>D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td><blockquote>
[!Note]<br />
Нет доступных API.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Мозаичный ресурс</td>
<td>D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
<tr class="even">
<td>Кодировщик видео</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</td>
</tr>
<tr class="odd">
<td>Многоплановый оверлей</td>
<td>D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</td>
<td>D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Уровни компонентов оборудования D3D12](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[**\_Поддержка формата \_ D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[**\_Формат D3D11 \_ SUPPORT2**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[Руководством по программированию для DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>


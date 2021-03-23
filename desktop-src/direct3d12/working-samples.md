---
title: Рабочие образцы
description: Рабочие образцы доступны для загрузки, показывая использование ряда функций Direct3D 12.
ms.assetid: 4C4475D4-534F-484F-8D60-9ACEA09AC109
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1b61ec374e21c9173797121ee90ec72e789de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103923"
---
# <a name="working-samples"></a>Рабочие образцы

Рабочие образцы доступны для загрузки, показывая использование ряда функций Direct3D 12.

## <a name="working-samples"></a>Рабочие образцы

Рабочие образцы (в виде проектов Visual Studio 2015) можно скачать на сайте [GitHub/Microsoft/DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples).

> [!Note]  
> Точный список выборок, доступных в этом расположении, будет зависеть от добавления и обновления образцов.

 



<table>
<thead>
<tr class="header">
<th>Пример заголовка</th>
<th>Описание</th>
<th>Классические приложения</th>
<th>UWP</th>
<th>Пошаговое руководство</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HelloWorld<dl> хелловиндов<br />
хеллотриангле<br />
хеллобундлес<br />
хеллоконстбуфферс<br />
хеллотекстуре<br />
</dl></td>
<td>Образец HelloWorld содержит следующие простые проекты, которые помогут приступить к работе с Direct3D 12.<dl> Создает окно при подготовке к просмотру содержимого Direct3D 12.<br />
Визуализирует простой треугольник с помощью Direct3D 12.<br />
Демонстрирует использование пакета для подготовки к просмотру с помощью Direct3D 12.<br />
Демонстрирует использование буферов констант для передачи данных в GPU, используемый для отрисовки в Direct3D 12.<br />
Демонстрирует применение текстуры к треугольнику с помощью Direct3D 12.<br />
</dl></td>
<td>Да</td>
<td>Да</td>
<td><a href="creating-a-basic-direct3d-12-component.md">Создание базового компонента Direct3D 12</a></td>
</tr>
<tr class="even">
<td>D3D12Bundles</td>
<td>Демонстрирует рекомендации по буферизации и синхронизации кадров, а также визуализацию простой сетки с помощью пакетов.</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="odd">
<td>D3D12Multithreading</td>
<td>Пример создания многопотокового приложения с поддержкой.</td>
<td>Да</td>
<td>N</td>

</tr>
<tr class="even">
<td>D3D12nBodyGravity</td>
<td>Демонстрируется использование нескольких ядер для выполнения асинхронных вычислений вместе с трехмерной работой на одном GPU.</td>
<td>Да</td>
<td>Да</td>
<td><a href="multi-engine-n-body-gravity-simulation.md">Моделирование притяжения на уровне "n-текст" для нескольких ядер</a></td>
</tr>
<tr class="odd">
<td>D3D12PredicationQueries</td>
<td>Демонстрирует перекрытияе отбора с помощью куч запросов и затенения.</td>
<td>Да</td>
<td>Да</td>
<td><a href="predication-queries.md">Запросы затенения</a></td>
</tr>
<tr class="even">
<td>D3D12DynamicIndexing</td>
<td>Демонстрирует возможности динамической индексации DirectX 12 и HLSL.</td>
<td>Да</td>
<td>Да</td>
<td><a href="dynamic-indexing-using-hlsl-5-1.md">Динамическое индексирование с помощью HLSL 5.1</a></td>
</tr>
<tr class="odd">
<td>D3D1211on12</td>
<td>Демонстрирует базовое использование слоя 11on12. В этом примере текст подготавливается с помощью D2D с помощью API Direct3D 11 на устройстве 11on12 Direct3D 12.</td>
<td>Да</td>
<td>Да</td>
<td><a href="d2d-using-d3d11on12.md">D2D с использованием D3D11on12</a></td>
</tr>
<tr class="even">
<td>D3D12ExecuteIndirect</td>
<td>Демонстрируется отбор подсистемы вычислений в сочетании с функцией "выполнить косвенную функцию" для отрисовки только тех объектов, которые прошли тест для отбора.</td>
<td>Да</td>
<td>Да</td>
<td><a href="indirect-drawing-and-gpu-culling-.md">Непрямое отображение и отбор GPU</a></td>
</tr>
<tr class="odd">
<td>D3D12PipelineStateCache</td>
<td>Демонстрирует кэширование объекта состояния конвейера (PSO).</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="even">
<td>D3D12Fullscreen</td>
<td>Демонстрирует, как выполнять обработку оконных переходов и изменение размера окна в DirectX 12.</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="odd">
<td>D3D12HeterogeneousMultiadapter</td>
<td>Демонстрирует, как совместно использовать рабочие нагрузки в нескольких графических процессорах разнородных с помощью общих куч.</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="even">
<td>D3D12ReservedResources</td>
<td>Демонстрирует использование зарезервированных (мозаичных) ресурсов. В этом примере для четырехъядерного ресурса используется зарезервированный ресурс, содержащий полную цепь MIP.</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="odd">
<td>D3D12Residency</td>
<td>Это решение с низкой стоимостью интеграции для управления кучами Direct3D 12 и фиксируемыми ресурсами с использованием методик управления памятью из Direct3D 11.</td>
<td>Да</td>
<td>Да</td>

</tr>
<tr class="even">
<td>D3D12SmallResources</td>
<td>Демонстрирует использование небольших размещенных ресурсов, в которых показана потенциальная экономия памяти, полученная с помощью размещенных ресурсов (с выравниванием по 4 КБ) над зафиксированными и зарезервированными ресурсами (с выравниванием по 64 КБ).</td>
<td>Да</td>
<td>Да</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Пошаговые инструкции по коду D3D12](d3d12-code-walk-throughs.md)
</dt> </dl>

 

 





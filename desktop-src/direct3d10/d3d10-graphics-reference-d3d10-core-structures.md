---
description: 'В этом разделе содержатся сведения о следующих основных структурах:'
ms.assetid: 84769515-3f3b-4464-9620-7b806bf905b3
title: Основные структуры Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de2260b108ea340a97f24acf61f6ae686e00342
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807954"
---
# <a name="direct3d-10-core-structures"></a>Основные структуры Direct3D 10

В этом разделе содержатся сведения о следующих основных структурах:



| Структуры                                                                               | Описание                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**D3D10 \_ Blend, \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)                                           | Параметры смешения для устройства Direct3D 10,0.                         |
| [**D3D10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)                                         | Параметры смешения для устройства Direct3D 10,1.                         |
| [**\_Поле D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)                                                          | Прямоугольная область, часто в текстуре.                            |
| [**D3D10 \_ счетчика \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_desc)                                       | Описание счетчика производительности.                                   |
| [**\_Сведения о счетчике D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_info)                                       | Сведения о возможностях счетчика производительности видеоадаптера. |
| [**D3D10 \_ \_ трафарета \_ глубины**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)                          | Описание трафарета глубины.                                         |
| [**D3D10 \_ глубина \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)                      | Операция с трафаретом глубины.                                           |
| [**\_ \_ Фильтр очереди D3D10 \_ info**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter)                            | Фильтр сообщений отладки.                                              |
| [**D3D10 \_ сведений \_ о \_ фильтре очереди \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc)                 | Описание фильтра сообщений отладки.                                  |
| [**\_Элемент ввода D3D10, \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                          | Описание элемента буфера вершин для входного слота.               |
| [**\_ \_ \_ Статистика конвейера данных D3D10 запросов \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_pipeline_statistics) | Статистика конвейерных запросов.                                           |
| [**D3D10 \_ запрос \_ данных \_ для \_ статистики**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_so_statistics)             | Потоковая передача статистики запросов этапа вывода.                                |
| [**Несвязанная \_ \_ \_ отметка времени данных запроса D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_timestamp_disjoint)   | Статистика запроса метки времени.                                          |
| [**D3D10 \_ запрос \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_desc)                                           | Описание запроса.                                                 |
| [**\_Сообщение D3D10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_message)                                                  | Сообщение отладки для информационной очереди.                           |
| [**D3D10 средство программной \_ прорисовки \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                 | Описание этапа растеризации.                                        |
| [**D3D10 \_ Rect**](d3d10-rect.md)                                                        | Плоский прямоугольник.                                                      |
| [**D3D10 \_ визуализации \_ целевого объекта \_ Blend \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)           | Параметры смешения для целевого объекта прорисовки Direct3D 10,1.                  |
| [**D3D10 \_ образец \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)                                       | Описание образца.                                               |
| [**\_Представление ресурсов шейдера D3D10 ( \_ \_ \_ DESC)**](/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc)           | Описание представления "шейдер — представление ресурсов" для Direct3D 10,0.                  |
| [**\_ \_ \_ DESC1 представления ресурсов шейдера \_ D3D10**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)         | Описание представления "шейдер — представление ресурсов" для Direct3D 10,1.                  |
| [**\_DESC параметра сигнатуры D3D10 \_ \_**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)              | Описание параметра шейдера.                                      |
| [**\_ \_ Маска блока состояния \_ D3D10**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask)                              | Маска блока состояния.                                                  |
| [**\_ \_ Запись объявления D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_so_declaration_entry)                      | Описание элемента буфера вершин для выходного слота.              |
| [**\_Окно просмотра D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)                                                | Размеры окна просмотра.                                                 |



 

Кроме того, в D3D10. h определена структура 2D Rectangle.


```
typedef RECT D3D10_RECT;
```



Документацию см. в разделе [Rect](/previous-versions//ms536136(v=vs.85)).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по основным](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 

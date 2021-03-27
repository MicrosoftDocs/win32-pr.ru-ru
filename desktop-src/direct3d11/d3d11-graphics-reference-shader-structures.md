---
title: Структуры шейдеров (графика Direct3D 11)
description: Структуры используются для создания и использования шейдеров.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- структуры, шейдеры Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800844"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Структуры шейдеров (графика Direct3D 11)

Структуры используются для создания и использования шейдеров.


## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                       | Описание                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**\_Экземпляр класса D3D11, \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Описывает экземпляр класса HLSL.<br/>                           |
| [**\_DESC D3D11 COMPUTE \_ Shader \_ Trace \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Описывает экземпляр шейдера вычислений для трассировки.<br/>         |
| [**\_ \_ DESC трассировки шейдера \_ домена \_ D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Описывает экземпляр шейдера домена для трассировки.<br/>          |
| [**D3D11 \_ функция \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Описывает функцию.<br/>                                       |
| [**\_DESC " \_ Трассировка шейдера D3D11 Geometry" \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Описывает экземпляр шейдера Geometry для трассировки.<br/>        |
| [**D3D11 \_ поверхности \_ Shader \_ Trace, \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Описывает экземпляр шейдера поверхности для трассировки.<br/>            |
| [**D3D11 \_ , \_ DESC, Библиотека**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Описывает библиотеку.<br/>                                        |
| [**\_DESC параметра \_ D3D11**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Описывает параметр функции. <br/>                            |
| [**\_DESC D3D11 \_ построителя \_ текстуры \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Описывает экземпляр шейдера пикселей для трассировки.<br/>           |
| [**\_DESC буфера шейдеров D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Описывает константный буфер шейдера.<br/>                         |
| [**Построитель текстуры D3D11, \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Описывает шейдер.<br/>                                         |
| [**\_ \_ \_ DESC входной привязки шейдера \_ D3D11**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Описывает привязку ресурса шейдера к входным данным шейдера.<br/> |
| [**\_DESC шейдера \_ D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Описывает объект трассировки шейдера.<br/>                            |
| [**\_Тип D3D11 шейдера " \_ \_ DESC"**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Описывает тип переменной шейдера.<br/>                           |
| [**D3D11ая \_ переменная шейдера \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Описывает переменную шейдера.<br/>                                |
| [**\_DESC параметра сигнатуры D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Описывает сигнатуру шейдера.<br/>                               |
| [**\_Регистр трассировки \_ D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Описывает регистр трассировки.<br/>                                 |
| [**\_Статистика трассировки \_ D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Указывает статистику трассировки.<br/>                         |
| [**\_Шаг трассировки \_ D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Описывает шаг трассировки, который является инструкцией.<br/>            |
| [**\_Значение трассировки \_ D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Описывает значение трассировки.<br/>                                    |
| [**\_DESC D3D11 вершинного \_ шейдера \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Описывает экземпляр шейдера вершин для трассировки.<br/>          |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по шейдерам](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 






---
description: Структуры, используемые для создания и использования ресурсов.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Структуры ресурсов (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701187"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Структуры ресурсов (графика Direct3D 10)

Структуры, используемые для создания и использования [ресурсов](d3d10-graphics-programming-guide-resources-types.md).



| Структуры                                                                 | Описание                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ буфер \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Описание ресурса [буфера](d3d10-graphics-programming-guide-resources-types.md) .                                                                     |
| [**\_РТВ буфера \_ D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Описывает элементы в [буфере](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.                                |
| [**D3D10 \_ буфера \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Описывает элементы в [буферном](d3d10-graphics-programming-guide-resources-types.md) ресурсе для использования в представлении ресурсов шейдера.                         |
| [**\_ \_ Представление набора элементов глубины D3D10, \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Описывает представление трафарета глубины.                                                                                                                               |
| [**D3D10, \_ сопоставленный \_ TEXTURE2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Предоставляет доступ к данным подресурсов в [двухмерной текстуре](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**D3D10, \_ сопоставленный \_ TEXTURE3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Предоставляет доступ к данным подресурсов в [трехмерной текстуре](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**\_ \_ Представление целевого объекта ПРОРИСОВКи D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Описывает представление целевого объекта рендеринга.                                                                                                                               |
| [**\_Данные о ПОДресурсе D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Указывает данные для инициализации ресурса.                                                                                                                   |
| [**Представление \_ \_ источника данных массива D3D10 TEX1D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Указывает, какой уровень mipmap и текстуры в [массиве с одномерной текстурой](d3d10-graphics-programming-guide-resources-types.md) используются в представлении трафарета глубины.       |
| [**D3D10 \_ TEX1D \_ array \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Указывает подресурсы из массива [одномерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.             |
| [**D3D10 \_ TEX1D \_ массив \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Задает уровни и текстуры mipmap в [массиве одномерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении "шейдер — представление ресурсов".      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Указывает вложенные ресурсы из [текстуры 1d](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении трафарета глубины.                        |
| [**D3D10 \_ TEX1D \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Указывает подресурсы из [одномерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Указывает подресурсы из [текстуры 1d](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.                      |
| [**Представление \_ \_ источника данных массива D3D10 TEX2D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Указывает, какой уровень mipmap и какие текстуры в [массиве 2D-текстур](d3d10-graphics-programming-guide-resources-types.md) используются в представлении трафарета глубины. |
| [**D3D10 \_ TEX2D \_ array \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Указывает, какой уровень mipmap и какие текстуры в [массиве 2D-текстур](d3d10-graphics-programming-guide-resources-types.md) используются в представлении целевого объекта визуализации. |
| [**D3D10 \_ TEX2D \_ массив \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Указывает подресурсы из массива [двумерных текстур](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Указывает вложенные ресурсы из [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении трафарета глубины.                        |
| [**D3D10 \_ TEX2D \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Указывает подресурсы из [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Указывает подресурсы из [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.                      |
| [**Представление \_ \_ источника данных массива D3D10 TEX2DMS \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Указывает подресурсы из массива [двумерных текстур](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении трафарета глубины.             |
| [**D3D10 \_ TEX2DMS \_ array \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Указывает подресурсы из массива [двумерных текстур](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.             |
| [**D3D10 \_ TEX2DMS \_ массив \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Указывает подресурсы из массива [двумерных текстур](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Указывает вложенные ресурсы из многовыборочной [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении трафарета глубины.           |
| [**D3D10 \_ TEX2DMS \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Указывает подресурсы из многовыборочной [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Указывает подресурсы из многовыборочной [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении "шейдер — представление ресурсов".         |
| [**D3D10 \_ TEX3D \_ РТВ**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Указывает подресурсы из [трехмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении целевого объекта визуализации.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Указывает подресурсы из [трехмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.                      |
| [**D3D10 \_ текскубе \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Указывает подресурсы из [текстуры Куба](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.                    |
| [**D3D10 \_ текскубе \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Указывает подресурсы из [текстуры Куба](d3d10-graphics-programming-guide-resources-types.md) для использования в представлении ресурсов шейдера.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Описывает ресурс [текстуры Немерного](d3d10-graphics-programming-guide-resources-types.md) типа.                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Описывает ресурс [двухмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Описывает ресурс [трехмерной текстуры](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на ресурс](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 




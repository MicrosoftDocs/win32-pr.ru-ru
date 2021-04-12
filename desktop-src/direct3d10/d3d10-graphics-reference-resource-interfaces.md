---
description: 'Direct3D 10 определяет ряд интерфейсов для двух основных типов ресурсов: буферов и текстур.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Интерфейсы ресурсов (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141355"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Интерфейсы ресурсов (графика Direct3D 10)

Direct3D 10 определяет ряд интерфейсов для двух основных типов ресурсов: [буферов](d3d10-graphics-programming-guide-resources-types.md) и текстур.



| Интерфейсы                                           | Описание                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Интерфейс ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Обращается к данным буфера.                                |
| [**Интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Базовый класс для ресурса.                           |
| [**Интерфейс ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Обращается к данным в виде одномерной текстуры или массива одномерной текстуры. |
| [**Интерфейс ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Обращается к данным в двухмерной текстуре или массиве 2D-текстур  |
| [**Интерфейс ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Обращается к данным в трехмерной текстуре или массиве трехмерной текстуры. |



 

Приложение использует представление для привязки ресурса к [этапу конвейера](d3d10-graphics-programming-guide-pipeline-stages.md). [Представление](d3d10-graphics-programming-guide-resources-access-views.md) определяет, как к ресурсу можно получить доступ во время подготовки к просмотру. API содержит эти интерфейсы представления.



| Интерфейсы                                                               | Описание                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Интерфейс ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Обращается к данным в текстуре [набора элементов глубины](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) . |
| [**Интерфейс ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Обращается к данным в [целевом объекте прорисовки](d3d10-graphics-programming-guide-resources-creating-textures.md).        |
| [**Интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Обращается к данным в шейдере — ресурсе в Direct3D 10,0.                                                         |
| [**Интерфейс ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Обращается к данным в шейдере — ресурсе в Direct3D 10,1.                                                         |
| [**Интерфейс ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Базовый класс для представления.                                                                                       |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на ресурс](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 

---
title: 'Интерфейсы шейдеров (графика Direct3D 11) '
description: В этом разделе содержатся сведения об интерфейсах шейдера.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- интерфейсы, шейдер Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479460"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Интерфейсы шейдеров (графика Direct3D 11) 

В этом разделе содержатся сведения об интерфейсах шейдера.

Каждый из этих интерфейсов шейдера управляет скомпилированным шейдером. Интерфейс создается при компиляции шейдера и передается различным интерфейсам API, которым требуется доступ к скомпилированному шейдеру. Например, при привязке шейдера к этапу конвейера или при получении сигнатуры шейдера.


## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Этот интерфейс инкапсулирует класс HLSL.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Этот интерфейс инкапсулирует динамическую компоновку HLSL.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Интерфейс шейдера вычислений управляет исполняемой программой (шейдером вычислений), которая управляет этапом COMPUTE-Shader.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Интерфейс шейдера домена управляет исполняемой программой (шейдером доменов), которая управляет стадией шейдера домена.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Интерфейс графа с функциями компоновки используется для создания шейдеров, состоящих из последовательности вызовов предкомпилированных функций, которые передают значения друг другу. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Интерфейс отражения функции обращается к сведениям о функции. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Интерфейс отражения параметров функции обращается к сведениям о параметрах функции. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Интерфейс шейдера Geometry управляет исполняемой программой (шейдером Geometry), которая управляет стадией шейдера Geometry.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Интерфейс шейдера поверхности управляет исполняемой программой (шейдером поверхности), которая управляет стадией поверхности-Shader.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Интерфейс отражения библиотеки обращается к сведениям о библиотеке. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Интерфейс компоновщика используется для связи модуля шейдера. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Для связывания с шейдером используется интерфейс связывания и узлов. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Интерфейс модуля создает экземпляр модуля, который используется для повторной привязки ресурсов. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Интерфейс экземпляра модуля используется для повторной привязки ресурсов. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Интерфейс построителя текстуры управляет исполняемой программой (построитель текстуры), которая управляет стадией построителя текстуры.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Интерфейс отражения шейдеров получает доступ к сведениям шейдера.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к буферу констант.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к типу переменной.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к переменной.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | Интерфейс <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> реализует методы для получения трассировок выполнения шейдера.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | Интерфейс <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> реализует метод для создания объектов сведений о трассировке шейдера.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Интерфейс шейдера вершин управляет исполняемой программой (вершинным шейдером), которая управляет стадией шейдера вершин.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по шейдерам](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 


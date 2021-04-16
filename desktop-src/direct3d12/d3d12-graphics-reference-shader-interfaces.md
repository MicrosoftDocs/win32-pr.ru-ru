---
title: Интерфейсы шейдера (графика Direct3D 12)
description: D3d12shader. h объявляет следующие интерфейсы.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- интерфейсы, шейдер Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105719184"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a>Интерфейсы шейдера (графика Direct3D 12)

d3d12shader. h объявляет следующие интерфейсы.

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
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br/></td>
<td>Интерфейс отражения параметров функции обращается к сведениям о параметрах функции. <br/>
<blockquote>
[!Note]<br />
Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br/></td>
<td>Интерфейс отражения функции обращается к сведениям о функции. <br/>
<blockquote>
[!Note]<br />
Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br/></td>
<td>Интерфейс отражения библиотеки обращается к сведениям о библиотеке. <br/>
<blockquote>
[!Note]<br />
Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br/></td>
<td>Интерфейс отражения шейдеров получает доступ к сведениям шейдера. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Этот интерфейс отражения шейдеров предоставляет доступ к буферу констант. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br/></td>
<td>Этот интерфейс отражения шейдеров предоставляет доступ к типу переменной. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br/></td>
<td>Этот интерфейс отражения шейдеров предоставляет доступ к переменной. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Справочник по шейдерам](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 






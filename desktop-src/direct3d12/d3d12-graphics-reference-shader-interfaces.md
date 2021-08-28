---
title: Интерфейсы шейдера (графика Direct3D 12)
description: D3d12shader. h объявляет следующие интерфейсы.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- интерфейсы, шейдер Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db734816efc14cb00b3e4254a4b39bc492f3b6e7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483180"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a>Интерфейсы шейдера (графика Direct3D 12)

d3d12shader. h объявляет следующие интерфейсы.

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br /> | Интерфейс отражения параметров функции обращается к сведениям о параметрах функции. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br /> | Интерфейс отражения функции обращается к сведениям о функции. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br /> | Интерфейс отражения библиотеки обращается к сведениям о библиотеке. <br /><blockquote>[!Note]<br />Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br /> | Интерфейс отражения шейдеров получает доступ к сведениям шейдера. <br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к буферу констант. <br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к типу переменной. <br /> | 
| <a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br /> | Этот интерфейс отражения шейдеров предоставляет доступ к переменной. <br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Справочник по шейдерам](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 






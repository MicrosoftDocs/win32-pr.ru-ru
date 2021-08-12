---
description: 'В этом разделе содержатся сведения о следующих интерфейсах:'
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: Интерфейсы эффектов (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07e6ecf45f4ef052c7d576849a55d00ef0f877dde7c41fa5dc80b7592761325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303977"
---
# <a name="effect-interfaces-direct3d-10"></a>Интерфейсы эффектов (Direct3D 10)

В этом разделе содержатся сведения о следующих интерфейсах:



| Интерфейсы                                                                                     | Описание                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Интерфейс ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | Доступ к состоянию смешения.                                            |
| [**Интерфейс ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Обращается к буферу текстуры или к константному буферу.                  |
| [**Интерфейс ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | Доступ к состоянию шаблона глубины.                                    |
| [**Интерфейс ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Обращается к представлению трафарета глубины.                                   |
| [**Интерфейс ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | Инкапсулирует состояние конвейера в одном или нескольких методах отрисовки. |
| [**Интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                                               | Реализованные пользователем методы для чтения включаемых файлов.              |
| [**Интерфейс ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | Обращается к матрице.                                               |
| [**Интерфейс ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | Инкапсулирует состояние воздействия в ходе прохода.                             |
| [**Интерфейс ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | Определяет переменные с общим действием.                              |
| [**Интерфейс ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | Доступ к состоянию средства отображения программной прорисовки.                                       |
| [**Интерфейс ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Обращается к объекту прорисовки.                                        |
| [**Интерфейс ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | Доступ к состоянию образца.                                          |
| [**Интерфейс ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | Обращается к скалярной переменной.                                      |
| [**Интерфейс ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Обращается к ресурсу шейдера.                                      |
| [**Интерфейс ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | Обращается к переменной шейдера.                                      |
| [**Интерфейс ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | Обращается к строке.                                               |
| [**Интерфейс ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | Инкапсулирует один или несколько проходов.                                 |
| [**Интерфейс ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | Реализует методы для доступа к переменным эффектов.               |
| [**Интерфейс ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | Обращается к вектору.                                               |



 

В платформе Effect существует два вида интерфейсов: интерфейсы отрисовки для отрисовки интерфейса эффектов и отражения для получения и установки переменных эффектов с помощью API. Все интерфейсы отражения являются производными от [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по действиям](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 

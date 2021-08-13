---
title: Effects 11, интерфейсы
description: В этом разделе содержатся справочные сведения о интерфейсах COM для источника Effects 11.
ms.assetid: 1b997513-73f7-423a-8af3-1c9fa0d2f469
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20713f5a40b2d8b85edb92166b7e64af18fefee62e5267adcffa25356c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537706"
---
# <a name="effects-11-interfaces"></a>Effects 11, интерфейсы

В этом разделе содержатся справочные сведения о интерфейсах COM для источника Effects 11.


## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                   | Описание                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)<br/>                                                       | Интерфейс [**ID3DX11Effect**](id3dx11effect.md) управляет набором объектов состояния, ресурсов и шейдеров для реализации результата отрисовки.<br/>                                                                                                                                                    |
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)<br/>                             | Интерфейс Blend-Variable получает доступ к состоянию смешения.<br/>                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)<br/>             | Обращается к экземпляру класса.<br/>                                                                                                                                                                                                                                                                         |
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)<br/>                           | Интерфейс постоянного буфера обращается к постоянным буферам или буферам текстур.<br/>                                                                                                                                                                                                                          |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)<br/>               | Интерфейс переменной с глубиной и набором элементов имеет доступ к состоянию шаблона глубины.<br/>                                                                                                                                                                                                                                   |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)<br/>       | Интерфейс "Глубина-трафарет-представление-переменная" обращается к представлению трафарета глубины.<br/>                                                                                                                                                                                                                             |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)<br/>                                             | Интерфейс [**ID3DX11EffectGroup**](id3dx11effectgroup.md) обращается к группе эффектов.<br/> Время существования объекта [**ID3DX11EffectGroup**](id3dx11effectgroup.md) равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .<br/>                               |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)<br/>                     | Обращается к переменной интерфейса.<br/>                                                                                                                                                                                                                                                                    |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)<br/>                           | Интерфейс переменной матрицы обращается к матрице.<br/>                                                                                                                                                                                                                                                     |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)<br/>                                               | Интерфейс [**ID3DX11EffectPass**](id3dx11effectpass.md) инкапсулирует назначения состояний в рамках метода.<br/> Время существования объекта [**ID3DX11EffectPass**](id3dx11effectpass.md) равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .<br/>           |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)<br/>                   | Интерфейс переменной средства прорисовки имеет доступ к состоянию программной прорисовки.<br/>                                                                                                                                                                                                                                         |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)<br/>       | Интерфейс представления визуализации-целевого объекта обращается к целевому объекту прорисовки.<br/>                                                                                                                                                                                                                                           |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)<br/>                         | Интерфейс образца имеет доступ к состоянию выборки.<br/>                                                                                                                                                                                                                                                        |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)<br/>                           | Интерфейс с скалярными переменными получает доступ к скалярным значениям.<br/>                                                                                                                                                                                                                                        |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)<br/>           | Интерфейс шейдера-ресурса получает доступ к ресурсу шейдера.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)<br/>                           | Интерфейс переменной шейдера обращается к переменной шейдера.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)<br/>                           | Интерфейс строковых переменных обращается к строковой переменной.<br/>                                                                                                                                                                                                                                            |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)<br/>                                     | Интерфейс [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) — это коллекция проходов.<br/> Время существования объекта [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .<br/>               |
| [**ID3DX11EffectType**](id3dx11effecttype.md)<br/>                                               | Интерфейс [**ID3DX11EffectType**](id3dx11effecttype.md) обращается к переменным эффектов по типу.<br/> Время существования объекта [**ID3DX11EffectType**](id3dx11effecttype.md) равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .<br/>                          |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)<br/> | Обращается к неупорядоченному представлению доступа.<br/>                                                                                                                                                                                                                                                                 |
| [**ID3DX11EffectVariable**](id3dx11effectvariable.md)<br/>                                       | Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) является базовым классом для всех переменных эффектов.<br/> Время существования объекта [**ID3DX11EffectVariable**](id3dx11effectvariable.md) равно времени существования родительского объекта [**ID3DX11Effect**](id3dx11effect.md) .<br/> |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)<br/>                           | Интерфейс векторной переменной обращается к вектору из четырех компонентов.<br/>                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по эффектам 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 






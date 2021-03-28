---
title: Системные интерфейсы эффектов (Direct3D 11)
description: Система эффектов определяет несколько интерфейсов для управления состоянием эффектов.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774081"
---
# <a name="effect-system-interfaces-direct3d-11"></a>Системные интерфейсы эффектов (Direct3D 11)

Система эффектов определяет несколько интерфейсов для управления состоянием эффектов. Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.

-   [Интерфейсы среды выполнения Effect](#effect-runtime-interfaces)
-   [Интерфейсы отражения эффектов](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Интерфейсы среды выполнения Effect

Использование интерфейсов среды выполнения для визуализации эффектов.



| Интерфейсы среды выполнения                                       | Описание                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**ID3DX11Effect**](id3dx11effect.md)                   | Коллекция одной или нескольких групп и методов для подготовки к просмотру. |
| [**ID3DX11EffectPass**](id3dx11effectpass.md)           | Коллекция назначений состояний.                             |
| [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md) | Коллекция из одного или нескольких проходов.                            |
| [**ID3DX11EffectGroup**](id3dx11effectgroup.md)         | Коллекция из одного или нескольких методов.                        |



 

## <a name="effect-reflection-interfaces"></a>Интерфейсы отражения эффектов

Отражение реализуется в системе эффектов для поддержки чтения (и записи) состояния воздействия. Существует несколько способов доступа к переменным эффектов.

### <a name="setting-groups-of-effect-state"></a>Установка групп состояния эффектов

Используйте эти интерфейсы для получения и установки группы состояний.



| Интерфейсы отражения                                                          | Описание                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)               | Получение и установка состояния смешения.         |
| [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md) | Возвращает и задает состояние шаблона глубины. |
| [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)     | Получение и установка состояния средства прорисовки.    |
| [**ID3DX11EffectSamplerVariable**](id3dx11effectsamplervariable.md)           | Получение и установка состояния образца.       |



 

### <a name="setting-effect-resources"></a>Настройка ресурсов эффектов

Используйте эти интерфейсы для получения и задания ресурсов.



| Интерфейсы отражения                                                                        | Описание                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)                           | Доступ к данным в буфере текстуры или буфере констант. |
| [**ID3DX11EffectDepthStencilViewVariable**](id3dx11effectdepthstencilviewvariable.md)       | Доступ к данным в ресурсе с набором элементов глубины.            |
| [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)       | Доступ к данным в целевом объекте прорисовки.                     |
| [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)           | Доступ к данным в ресурсе шейдера.                   |
| [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md) | Доступ к данным в представлении неупорядоченного доступа.            |



 

### <a name="setting-other-effect-variables"></a>Задание других переменных эффектов

Используйте эти интерфейсы для получения и задания состояния по типу переменной.



| Интерфейсы отражения                                                            | Описание               |
|----------------------------------------------------------------------------------|---------------------------|
| [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) | Получение экземпляра класса.     |
| [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)         | Получение и установка интерфейса. |
| [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)               | Получение и задание матрицы.     |
| [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)               | Получение и задание скаляра.     |
| [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)               | Получение переменной шейдера.    |
| [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)               | Возвращает и задает строку.     |
| [**ID3DX11EffectType**](id3dx11effecttype.md)                                   | Получение типа переменной.      |
| [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)               | Возвращает и задает вектор.     |



 

Все интерфейсы отражения являются производными от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Руководство по программированию для Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





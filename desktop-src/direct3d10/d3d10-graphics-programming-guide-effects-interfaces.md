---
description: 'Система эффектов определяет несколько интерфейсов для управления состоянием эффектов. Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Системные интерфейсы эффектов (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141202"
---
# <a name="effect-system-interfaces-direct3d-10"></a>Системные интерфейсы эффектов (Direct3D 10)

Система эффектов определяет несколько интерфейсов для управления состоянием эффектов. Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.

-   [Интерфейсы среды выполнения Effect](#effect-runtime-interfaces)
-   [Интерфейсы отражения эффектов](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a>Интерфейсы среды выполнения Effect

Использование интерфейсов среды выполнения для визуализации эффектов.



| Интерфейсы среды выполнения                                               | Описание                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Интерфейс ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | Коллекция из одного или нескольких методов для отрисовки.                  |
| [**Интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))                 | Интерфейс для добавления пользовательских поведений при чтении включаемых файлов. |
| [**Интерфейс ID3D10EffectPass**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | Коллекция назначений состояний.                                   |
| [**Интерфейс ID3D10EffectPool**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | Создайте место в памяти для переменных, которые будут совместно использоваться различными эффектами. |
| [**Интерфейс ID3D10EffectTechnique**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | Коллекция из одного или нескольких проходов.                                  |



 

## <a name="effect-reflection-interfaces"></a>Интерфейсы отражения эффектов

Отражение реализуется в системе эффектов для поддержки чтения (и записи) состояния воздействия. Существует несколько способов доступа к переменным эффектов.

### <a name="setting-groups-of-effect-state"></a>Установка групп состояния эффектов

Используйте эти интерфейсы для получения и установки группы состояний.



| Интерфейсы отражения                                                                  | Описание                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [**Интерфейс ID3D10EffectBlendVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | Получение и установка состояния смешения.         |
| [**Интерфейс ID3D10EffectDepthStencilVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | Возвращает и задает состояние шаблона глубины. |
| [**Интерфейс ID3D10EffectRasterizerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | Получение и установка состояния средства прорисовки.    |
| [**Интерфейс ID3D10EffectSamplerVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | Получение и установка состояния образца.       |



 

### <a name="setting-effect-resources"></a>Настройка ресурсов эффектов

Используйте эти интерфейсы для получения и задания ресурсов.



| Интерфейсы отражения                                                                          | Описание                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [**Интерфейс ID3D10EffectConstantBuffer**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | Доступ к данным в буфере текстуры или буфере констант. |
| [**Интерфейс ID3D10EffectDepthStencilViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | Доступ к данным в ресурсе с набором элементов глубины.            |
| [**Интерфейс ID3D10EffectRenderTargetViewVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | Доступ к данным в целевом объекте прорисовки.                     |
| [**Интерфейс ID3D10EffectShaderResourceVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | Доступ к данным в ресурсе шейдера.                   |



 

### <a name="setting-other-effect-variables"></a>Задание других переменных эффектов

Используйте эти интерфейсы для получения и задания состояния по типу переменной.



| Интерфейсы отражения                                                      | Описание                    |
|----------------------------------------------------------------------------|--------------------------------|
| [**Интерфейс ID3D10EffectMatrixVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | Получение и задание матрицы.          |
| [**Интерфейс ID3D10EffectScalarVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | Получение и задание скаляра.          |
| [**Интерфейс ID3D10EffectShaderVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | Возвращает и задает переменную шейдера. |
| [**Интерфейс ID3D10EffectStringVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | Возвращает и задает строку.          |
| [**Интерфейс ID3D10EffectType**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | Получение типа переменной.           |
| [**Интерфейс ID3D10EffectVectorVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | Возвращает и задает вектор.          |



 

Все интерфейсы отражения являются производными от [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[Рекомендации по программированию для Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 

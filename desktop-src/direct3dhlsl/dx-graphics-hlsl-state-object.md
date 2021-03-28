---
title: Объекты состояния
description: Используйте HLSL для определения объектов State.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998010"
---
# <a name="state-objects"></a>Объекты состояния

С помощью моделей шейдеров 6,3 и более поздних версий приложения имеют удобную и гибкую возможность определения объектов состояния ДКСР непосредственно в коде шейдера HLSL в дополнение к использованию API-интерфейсов Direct3D 12.

В HLSL объекты состояния объявляются с помощью этого синтаксиса:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**<br/>     | Определяет тип подобъекта. Должен быть одним из поддерживаемых типов подобъектов HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Поле [1, 2,...]**<br/> | Поля подобъекта. Ниже описаны конкретные поля для каждого типа подобъекта.<br/> |




Список типов подобъектов:
-   [статеобжектконфиг](#stateobjectconfig)
-   [глобалрутсигнатуре](#globalrootsignature)
-   [локалрутсигнатуре](#localrootsignature)
-   [субобжекттоекспортсассокатион](#subobjecttoexportsassocation)
-   [райтраЦингшадерконфиг](#raytracingshaderconfig)
-   [райтраЦингпипелинеконфиг](#raytracingpipelineconfig)
-   [трианглехитграуп](#trianglehitgroup)
-   [процедуралпримитивехитграуп](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>статеобжектконфиг

Тип подобъекта Статеобжектконфиг соответствует структуре [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .

У него есть одно поле, побитовый флаг, который является одним или обоими

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

или ноль ни для одного из них.

Пример

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>глобалрутсигнатуре
Глобалрутсигнатуре соответствует структуре [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .

Поля состоят из нескольких строк, описывающих части корневой сигнатуры. Справочные сведения об этом см. [в разделе Указание корневых подписей в HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Пример
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>локалрутсигнатуре
Локалрутсигнатуре соответствует структуре [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .

Как и в случае с глобальным корневым объектом подписи, поля состоят из нескольких строк, описывающих части корневой сигнатуры. Справочные сведения об этом см. [в разделе Указание корневых подписей в HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Пример
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>субобжекттоекспортсассокатион
По умолчанию подобъект, только объявленный в той же библиотеке, что и экспорт, может применяться к этому экспорту. Однако приложения имеют возможность переопределить это и получить конкретные сведения о том, какой из них выполняет экспорт. В HLSL это "явная ассоциация" выполняется с помощью Субобжекттоекспортсассокатион.

Субобжекттоекспортсассокатион соответствует структуре [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .

Этот подобъект объявляется с помощью синтаксиса

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**субобжектнаме**<br/>     | Строка, определяющая экспортированный подобъект.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Экспорт**<br/> | Строка, содержащая разделенный точками с запятой список экспортов.<br/> |


Пример
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Обратите внимание, что в обоих полях используются *экспортированные* имена. Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.

## <a name="raytracingshaderconfig"></a>райтраЦингшадерконфиг

РайтраЦингшадерконфиг соответствует структуре [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .

Этот подобъект объявляется с помощью синтаксиса

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**макспайлоадсизе**<br/>     | Числовое значение для максимального хранилища для скаляров (подсчитывается как 4 байта каждый) в полезных данных лучей для связанных шейдеров райтраЦинг.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**максаттрибутесизе**<br/> | Числовое значение для максимального числа скаляров (подсчитывается как 4 байта), которое может использоваться для атрибутов в связанных шейдерах райтраЦинг. Значение не может превышать [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Пример
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>райтраЦингпипелинеконфиг

РайтраЦингпипелинеконфиг соответствует структуре [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .

Этот подобъект объявляется с помощью синтаксиса

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**макстрацерекурсиондепс**<br/>     | Числовой предел, используемый для рекурсии лучей в конвейере райтраЦинг. Это число от 0 до 31 включительно. <br/> |


Пример
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Так как для рекурсии райтраЦинг существуют затраты на производительность, приложения должны использовать минимальную глубину рекурсии, необходимую для нужных результатов.

Если вызовы шейдера еще не достигли максимальной глубины рекурсии, они могут вызывать [трацерай](../direct3d12/traceray-function.md) любое количество раз. Но если они достигли или превышают максимальную глубину рекурсии, вызов Трацерай переводит устройство в состояние «удалено». Таким образом, шейдеры райтраЦинг должны отказаться от вызова Трацерай, если они удовлетворены или превысили максимальную глубину рекурсии.

## <a name="trianglehitgroup"></a>трианглехитграуп

Трианглехитграуп соответствует структуре [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) , для которой в поле Type задано значение [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Этот подобъект объявляется с помощью синтаксиса

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**анихитшадер**<br/>     | Строковое имя шейдера анихит для группы попаданий или пустая строка.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**клосесситшадер**<br/> | Строковое имя ближайшего шейдера нажатия для группы попаданий или пустая строка.<br/> |


Пример
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Обратите внимание, что в обоих полях используются *экспортированные* имена. Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.

## <a name="proceduralprimitivehitgroup"></a>процедуралпримитивехитграуп

Процедуралпримитивехитграуп соответствует структуре [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) , для которой в поле Type задано значение [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Этот подобъект объявляется с помощью синтаксиса

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Элемент                                                                                         | Описание                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/>     | Строка ASCII, однозначно определяющая имя переменной.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**анихитшадер**<br/>     | Строковое имя шейдера анихит для группы попаданий или пустая строка.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**клосесситшадер**<br/> | Строковое имя ближайшего шейдера нажатия для группы попаданий или пустая строка.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**интерсектионшадер**<br/> | Строковое имя шейдера пересечения для группы попаданий или пустая строка.<br/> |


Пример
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Обратите внимание, что в трех полях используются *экспортированные* имена. Экспортированное имя может отличаться от исходного имени в HLSL, если приложение выбирает экспорт-переименование.

## <a name="remarks"></a>Примечания

Подобъекты имеют понятие "Ассоциация" или "какой подобъект проходит с помощью экспорта".

При указании подобъектов с помощью кода шейдера выбирается параметр «какой подобъект проходит с экспортом» согласно правилам, описанным в [спецификации дкср](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). В частности, предположим, что в приложении есть экспорт. Если приложение связывается с экспортом с корневой подписью A с помощью шейдера и корневой сигнатуры B с помощью кода приложения, то используется именно объект B. Проектирование «использование B» вместо «создание ошибки» дает приложениям возможность удобно переопределять ассоциации ДКСИЛ с помощью кода приложения, а не принудительно перекомпилировать шейдеры для устранения несоответствий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись блога разработчиков DirectX: "Новая возможность в D3D12 — DirectX РайтраЦинг (ДКСР) теперь поддерживает подобъекты библиотеки"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Функциональная спецификация DirectX РайтраЦинг (ДКСР)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Пример: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>
---
title: Создание корневой подписи
description: Корневые подписи являются сложной структурой данных, содержащей вложенные структуры.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548946"
---
# <a name="creating-a-root-signature"></a>Создание корневой подписи

Корневые подписи являются сложной структурой данных, содержащей вложенные структуры. Их можно определить программно с помощью приведенного ниже определения структуры данных (в том числе методы для помощи в инициализации членов). Кроме того, они могут быть созданы на языке высокого уровня заливки (HLSL), что дает возможность компилятору проверять, что макет совместим с шейдером.

API для создания корневой подписи принимает сериализованную (автономную) версию описания макета, описанную ниже. Метод предназначен для создания этой сериализованной версии из структуры данных C++, но другим способом получения сериализованного определения корневой подписи является получение его из шейдера, скомпилированного с помощью корневой подписи.

Если вы хотите воспользоваться преимуществами оптимизации драйверов для дескрипторов корневых подписей и данных, обратитесь к [корневой сигнатуре версии 1,1](root-signature-version-1-1.md) .

-   [Типы привязки таблицы дескрипторов](#descriptor-table-bind-types)
-   [Диапазон дескрипторов](#descriptor-range)
-   [Макет таблицы дескрипторов](#descriptor-table-layout)
-   [Корневые константы](#root-constants)
-   [Дескриптор корня](#root-descriptor)
-   [Видимость шейдера](#shader-visibility)
-   [Определение корневой подписи](#root-signature-definition)
-   [Сериализация и десериализация структуры данных корневой подписи](/windows)
-   [API создания корневой подписи](#root-signature-creation-api)
-   [Корневая подпись в объектах состояния конвейера](#root-signature-in-pipeline-state-objects)
-   [Код для определения корневой сигнатуры версии 1,1](#code-for-defining-a-version-11-root-signature)
-   [Связанные темы](#related-topics)

## <a name="descriptor-table-bind-types"></a>Типы привязки таблицы дескрипторов

[**\_ \_ \_ Тип диапазона дескрипторов перечисления D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) определяет типы передескрипторов, на которые может ссылаться как часть определения макета таблицы дескрипторов.

Это диапазон, так что, например, если часть таблицы дескрипторов имеет 100 СРВС, этот диапазон можно объявить в одной записи, а не в 100. Поэтому определение таблицы дескрипторов — это коллекция диапазонов.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Диапазон дескрипторов

Структура [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) определяет набор дескрипторов заданного типа (например, СРВС) в таблице дескрипторов.

Этот `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` макрос обычно можно использовать для `OffsetInDescriptorsFromTableStart` параметра [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Это означает, что добавляется диапазон дескрипторов, определенный после предыдущего в таблице дескрипторов. Если приложению требуется создать псевдонимы для дескрипторов или по какой-либо причине нужно пропускать слоты, для него можно задать `OffsetInDescriptorsFromTableStart` любое смещение. Определение перекрывающихся диапазонов различных типов недопустимо.

Набор регистров шейдеров, заданный сочетанием `RangeType` ,, и, `NumDescriptors` `BaseShaderRegister` `RegisterSpace` не может конфликтовать или перекрывать любые объявления в корневой сигнатуре, которые имеют общую [**\_ \_ видимость шейдера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (см. раздел видимость шейдера ниже).

## <a name="descriptor-table-layout"></a>Макет таблицы дескрипторов

Структура [**\_ \_ \_ таблицы дескрипторов root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) объявляет макет таблицы дескрипторов в виде коллекции диапазонов дескрипторов, которые появляются в куче дескрипторов один за другим. Пробы не разрешены в той же таблице дескрипторов, что и CBV/UAV/СРВС.

Эта структура используется, если для корневого слота подписи задано значение `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Чтобы задать таблицу дескрипторов графики (CBV, SRV, UAV, образец), используйте [**ID3D12GraphicsCommandList:: сетграфиксрутдескриптортабле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Чтобы задать таблицу дескрипторов вычислений, используйте [**ID3D12GraphicsCommandList:: сеткомпутерутдескриптортабле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Корневые константы

Структура [**\_ \_ констант D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) объявляет константы встроенной в корневой сигнатуре, которая отображается в шейдере как один буфер константы.

Эта структура используется, если для корневого слота подписи задано значение `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Дескриптор корня

Структура [**\_ корневого \_ дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) в качестве встроенной сигнатуры объявляет дескрипторы (которые отображаются в шейдере).

Эта структура используется, если тип слота корневой подписи имеет значение `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` или `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Видимость шейдера

Член набора перечисления [**\_ \_ видимости шейдеров D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) , заданный в параметре видимости шейдера [**\_ \_ параметра root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) , определяет, какие шейдеры видят содержимое заданного корневого слота подписи. Функция COMPUTE всегда использует \_ ALL (так как имеется только один активный этап). График может выбрать, но если в ней используются \_ все, то все этапы построителя текстур видят все, что привязано к корневому слоту подписи.

Один из способов использования видимости шейдеров — помочь с шейдерами, созданными в ожидании различных привязок на каждый этап шейдера с помощью перекрывающихся пространств имен. Например, шейдер вершин может объявлять:

 

Texture2D foo: Register (T0); "

 

Кроме того, шейдер пикселей может также объявлять:

 

Texture2D линейчатая: Register (T0);

Если приложение делает привязку корневой подписи для T0 видимости \_ все, обе шейдеры видят одну и ту же текстуру. Если шейдер определяет, что каждый шейдер должен видеть различные текстуры, он может определить два корневых слота подписи с \_ вершиной видимости и \_ пикселями. Независимо от того, какая область видимости находится в корневом слоте подписи, она всегда имеет такие же затраты (только в зависимости от того, что Слоттипе) в сторону одного фиксированного максимального размера корневой подписи.

На низком D3D11 оборудовании видимость ШЕЙДЕРа также учитывается \_ при проверке размеров таблиц дескрипторов в корневом макете, так как некоторые D3D11 оборудование могут поддерживать только максимальное количество привязок на каждый этап. Эти ограничения накладываются только при работе на оборудовании низкого уровня и не ограничивают более современное оборудование.

Если в корневой сигнатуре определено несколько таблиц дескрипторов, которые перекрывают друг друга в пространстве имен (привязки регистров к шейдеру), а любой из них указывает \_ все для видимости, то макет является недопустимым (создание завершится ошибкой).

## <a name="root-signature-definition"></a>Определение корневой подписи

[**Корневая структура \_ \_ подписи \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) может содержать таблицы дескрипторов и встроенные константы, каждый тип слота, определенный структурой [**\_ \_ параметра D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) , и [**\_ \_ \_ тип корневого параметра enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).

Чтобы инициировать корневой слот подписи, см. методы **сеткомпутерут \* \* \*** и **сетграфиксрут \* \* \*** в [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Статические пробы описаны в корневой подписи с использованием [**структуры \_ статического \_ образца D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

Некоторые флаги ограничивают доступ определенных шейдеров к корневой подписи, см. [**\_ \_ \_ Флаги корневой сигнатуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Сериализация и десериализация структуры данных корневой подписи

Методы, описанные в этом разделе, экспортируются с помощью D3D12Core.dll и предоставляют методы для сериализации и десериализации корневой структуры данных сигнатуры.

Сериализованная форма передается в API при создании корневой подписи. Если шейдер был создан с помощью корневой подписи (при добавлении этой возможности), скомпилированный шейдер уже будет содержать сериализованную корневую подпись.

Если приложение последовательно создает структуру данных [**D3D12 \_ корневой \_ подписи \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , она должна сделать сериализованную форму с помощью [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). Выходные данные, которые можно передать в [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Если у приложения уже есть сериализованная корневая подпись или скомпилированный шейдер, содержащий корневую подпись и желающий программно обнаружить Определение макета (называемое "отражением"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) можно вызвать. При этом создается интерфейс [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , который содержит метод, возвращающий десериализованную структуру данных [**\_ DESC корневой \_ сигнатуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) . Интерфейс владеет жизненным циклом десериализованной структуры данных.

## <a name="root-signature-creation-api"></a>API создания корневой подписи

API [**ID3D12Device:: креатерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) принимает сериализованную версию корневой сигнатуры.

## <a name="root-signature-in-pipeline-state-objects"></a>Корневая подпись в объектах состояния конвейера

Методы для создания состояния конвейера ([**ID3D12Device:: креатеграфикспипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) и [**ID3D12Device:: креатекомпутепипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) принимают необязательный интерфейс [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) в качестве входного параметра (который хранится в структуре описания [**\_ \_ \_ состояния \_ графического конвейера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ). Все корневые подписи, уже имеющиеся в шейдере, переопределяются.

Если корневая подпись передается в один из методов создания состояния конвейера, эта корневая подпись проверяется по всем шейдерам в PSO на совместимость и передается драйверу для использования со всеми шейдерами. Если какой-либо из шейдеров имеет другую корневую подпись, он заменяется корневой подписью, передаваемой в API. Если корневая подпись не передается, все передаваемые шейдеры должны иметь корневую подпись и должны совпадать — это будет предоставлено драйверу. Установка PSO для списка команд или набора не приводит к изменению корневой подписи. Это достигается с помощью методов [**сетграфиксрутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) и [**сеткомпутерутсигнатуре**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). При вызове времени (Graphics)/диспатч (вычисление) приложение должно гарантировать, что текущая PSO соответствует текущей корневой сигнатуре. в противном случае поведение не определено.

## <a name="code-for-defining-a-version-11-root-signature"></a>Код для определения корневой сигнатуры версии 1,1

В приведенном ниже примере показано, как создать корневую подпись в следующем формате:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **рутпараметериндекс** | **Contents**                                   |                                              |
| \[0\]                  | Корневые константы: {B2}                         | (1 CBV)                                      |
| \[1\]                  | Таблица дескрипторов: {T2-T7, U0-U3}             | (6 СРВС + 4 Уавс)                            |
| \[2\]                  | Корневой CBV: {B0}                               | (1 CBV, статические данные)                         |
| \[3\]                  | Таблица дескрипторов: {S0-S1}                    | (2 проба)                                 |
| \[4\]                  | Таблица дескрипторов: {T8-unbound}           | (без ограничений \# СРВС, переменных дескрипторов) |
| \[5\]                  | Таблица дескрипторов: {(T0, space1) — без ограничений} | (без ограничений \# СРВС, переменных дескрипторов) |
| \[6\]                  | Таблица дескрипторов: {B1}                       | (1 CBV, статические данные)                         |



 

Если большинство частей корневой подписи используются в большинстве случаев, это может быть лучше, чем необходимость слишком частого переключения корневой подписи. Приложения должны сортировать записи в корневой сигнатуре от наиболее часто изменяющихся по меньшей мере. Когда приложение изменяет привязки на любую часть корневой сигнатуры, драйверу может потребоваться создать копию некоторых или всех состояний корневой подписи, что может стать нетривиальной стоимостью при умножении нескольких изменений состояния.

Кроме того, в корневой подписи будет определена статическая выборка, которая выполняет анизотропную фильтрацию текстур при регистрации шейдера в регистре S3.

После привязки этой корневой сигнатуры таблицы дескрипторов, корневые CBV и константы могут быть назначены в \[ пространстве параметров 0.. 6 \] . Например, таблицы дескрипторов (диапазоны в куче дескрипторов) можно привязать к каждому из корневых параметров \[ 1 \] и \[ 3.. 6 \] .

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

В следующем коде показано, как указанная выше подпись может использоваться в списке команд графики.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Корневые подписи](root-signatures.md)
</dt> <dt>

[Указание корневых подписей в HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Использование корневой подписи](using-a-root-signature.md)
</dt> </dl>

 

 

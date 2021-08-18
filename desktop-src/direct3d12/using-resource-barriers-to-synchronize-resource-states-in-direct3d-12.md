---
title: Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12
description: Чтобы снизить общую загрузку ЦП и включить многопотоковую обработку и поддержку драйвера, Direct3D 12 перенесет ответственность за управление состоянием каждого ресурса из драйвера графики в приложение.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f79d5463c2f27560049f785b5cc32fe42ae33927cba7d039b90638f3946531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989434"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12

Чтобы снизить общую загрузку ЦП и включить многопотоковую обработку и поддержку драйвера, Direct3D 12 перенесет ответственность за управление состоянием каждого ресурса из драйвера графики в приложение. Пример состояния для каждого ресурса — указывает, осуществляется ли доступ к ресурсу текстуры в данный момент как через шейдер представление ресурсов или как представление целевого объекта прорисовки. В Direct3D 11 для отслеживания этого состояния в фоновом режиме были необходимы драйверы. Это дорого с точки зрения ЦП и существенно усложняется при любом многопоточном проектировании. В Microsoft Direct3D 12 большая часть состояния каждого ресурса управляется приложением с одним API, [**ID3D12GraphicsCommandList:: ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Использование API Ресаурцебарриер для управления состоянием каждого ресурса](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Состояния ресурсов](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Начальные состояния для ресурсов](#initial-states-for-resources)
    -   [Ограничения состояния ресурсов для чтения и записи](#readwrite-resource-state-restrictions)
    -   [Состояния ресурсов для представления задних буферов](#resource-states-for-presenting-back-buffers)
    -   [Отмена ресурсов](#discarding-resources)
-   [Неявные переходы состояний](#implicit-state-transitions)
    -   [Повышение общего состояния](#common-state-promotion)
    -   [Decay состояния для общего](#state-decay-to-common)
    -   [Влияние на производительность](#performance-implications)
-   [Разделите барьеры](#split-barriers)
-   [Пример сценария барьера ресурсов](#resource-barrier-example-scenario)
-   [Пример повышения общего состояния и Decay](#common-state-promotion-and-decay-sample)
-   [Пример разделенных барьеров](#example-of-split-barriers)
-   [Связанные темы](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Использование API Ресаурцебарриер для управления состоянием каждого ресурса

[**Ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) уведомляет графический драйвер о ситуациях, в которых драйверу может потребоваться синхронизировать несколько обращений к памяти, в которой хранится ресурс. Метод вызывается с одной или несколькими структурами описания барьера ресурсов, которые указывают тип объявляемого барьера ресурсов.

Существует три типа барьеров ресурсов:

-   **Барьер перехода** . барьер перехода указывает, что набор подресурсов переходит между различными использованиями. Структура [**\_ \_ \_ барьера переключения ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) используется для указания подресурса, который перемещается, а также состояний *до* и *после* подресурсов.

    Система проверяет, что переходы между подресурсами в списке команд соответствуют предыдущим переходам в том же списке команд. Слой отладки дополнительно отслеживает состояние подресурсов для поиска других ошибок, однако эта проверка является консервативной и не является исчерпывающей.

    Обратите внимание, что можно использовать \_ флаг D3D12 ресурсов " \_ \_ все \_ подресурсы", чтобы указать, что перемещаются все подресурсы в ресурсе.

-   **Барьер псевдонима** . барьер псевдонима указывает переход между использованием двух разных ресурсов, которые имеют перекрывающиеся сопоставления в одну кучу. Это относится как к зарезервированным, так и к размещенным ресурсам. Структура [**\_ \_ \_ барьера с псевдонимами ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) используется для указания ресурсов *Before* и *After* .

    Обратите внимание, что один или оба ресурса могут иметь значение NULL, что означает, что любой мозаичный ресурс может вызвать присвоение псевдонимов. Дополнительные сведения об использовании мозаичных ресурсов см. в разделе [мозаичные](../direct3d11/tiled-resources.md) ресурсы и [ресурсы мозаики тома](volume-tiled-resources.md).

-   **Неупорядоченное представление доступа (UAV)** . барьер UAV указывает, что все доступ UAV (чтение или запись) к определенному ресурсу должно быть завершено между любыми последующими UAV доступом, как для чтения, так и для записи. Приложение не обязательно помещает UAV барьер между двумя вызовами Draw или Dispatch, которые считывают только из UAV. Кроме того, нет необходимости поUAV барьер между двумя вызовами Draw или Dispatch, которые выполняют запись в один и тот же UAV, если приложение знает, что можно обеспечить безопасность доступа UAV в любом порядке. Структура [**\_ \_ \_ барьера UAV ресурсов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) используется для указания ресурса UAV, к которому применяется барьер. Приложение может указать значение NULL для UAV барьера, что означает, что любой доступ UAV может потребовать барьера.

При вызове [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) с массивом описаний барьера ресурсов API ведет себя так, как если бы он вызывался для каждого элемента в том порядке, в котором они были предоставлены.

В любой момент времени подресурс находится в одном состоянии, определяемом набором флагов [**\_ \_ состояний ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) , предоставленных для [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier). Приложение должно гарантировать, что состояния *Before* и *After* последовательных вызовов **ресаурцебарриер** согласуются.

> [!TIP]
>
> По возможности приложения должны объединять несколько переходов в один вызов API.

 

### <a name="resource-states"></a>Состояния ресурсов

Полный список состояний ресурсов, между которыми может переходить ресурс, см. в справочном разделе о перечислении [**\_ \_ состояний ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

Для раздельных барьеров ресурсов также можно использовать [**\_ \_ \_ Флаги D3D12 Resource барьера**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Начальные состояния для ресурсов

Ресурсы могут быть созданы с любым пользовательским начальным состоянием (допустимо для описания ресурса) со следующими исключениями.

-   Uploadные кучи должны начинаться в состоянии ресурса D3D12 \_ \_ \_ универсальное \_ чтение, которое является побитовым или сочетанием:
    -   D3D12 \_ \_ \_ вершину \_ и \_ буфер постоянного \_ состояния ресурса
    -   \_ \_ \_ Буфер индекса состояния ресурса \_ D3D12
    -   \_ \_ \_ Источник копирования состояния ресурса \_ D3D12
    -   Ресурс D3D12 с \_ \_ состоянием ресурса \_ \_ шейдер не пикселей \_ \_
    -   \_ \_ \_ \_ Ресурс построителя текстуры состояния ресурса \_ D3D12
    -   \_ \_ \_ Косвенный аргумент состояния ресурса D3D12 \_
-   Реадбакк кучи должны начинаться в \_ состоянии ресурса D3D12 \_ копирование состояния \_ \_ приемника.
-   Буферы обратного переключения цепочки автоматически запускаются в \_ общем состоянии "состояние ресурса D3D12" \_ \_ .

Прежде чем кучу может быть целевым объектом операции копирования GPU, обычно куча должна быть переведена в \_ \_ \_ состояние приемника D3D12 для копирования состояния ресурса \_ . Тем не менее ресурсы, созданные в кучах отправки, должны запускаться и не могут измениться из общего \_ состояния чтения, так как только процессор будет выполнять запись. И наоборот, зафиксированные ресурсы, созданные в кучах РЕАДБАКК, должны запускаться в и не могут изменяться из \_ состояния приемника копирования.

### <a name="readwrite-resource-state-restrictions"></a>Ограничения состояния ресурсов для чтения и записи

Биты использования состояния ресурсов, которые используются для описания состояния ресурса, делятся на состояния "только для чтения" и "чтение/запись". В справочном разделе, посвященном [**\_ \_ состояниям ресурсов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) , указывается уровень доступа для чтения и записи для каждого бита в перечислении.

Для любого ресурса можно задать только один бит чтения и записи. Если задан бит записи, для этого ресурса не может быть установлен бит, доступный только для чтения. Если бит записи не задан, может быть задано любое число бит чтения.

### <a name="resource-states-for-presenting-back-buffers"></a>Состояния ресурсов для представления задних буферов

Перед выводом заднего буфера он должен находиться в \_ общем состоянии ресурса D3D12 \_ \_ . Обратите внимание, что состояние ресурса D3D12 \_ ресурсов \_ \_ представляет собой синоним для \_ состояния ресурса \_ D3D12 \_ Common, и оба они имеют значение 0. Если [**идксгисвапчаин::P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) повторная отправка (или [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) вызывается для ресурса, который в настоящее время не находится в этом состоянии, выдается предупреждение слоя отладки.

### <a name="discarding-resources"></a>Отмена ресурсов

Все подресурсы в ресурсе должны находиться в \_ состоянии целевого объекта прорисовки или в глубине \_ записи для целевых объектов отрисовки и ресурсов трафарета глубины соответственно, при вызове [**ID3D12GraphicsCommandList::D искардресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .

## <a name="implicit-state-transitions"></a>Неявные переходы состояний

Ресурсы могут быть "более продвинутыми" из \_ состояния ресурса D3D12 " \_ Общее" \_ . Аналогичным образом ресурсы будут иметь значение "Decay", чтобы D3D12 \_ состояние ресурса " \_ Общее" \_ .

### <a name="common-state-promotion"></a>Повышение общего состояния

Все буферные ресурсы, а также текстуры с \_ \_ флагом ресурса D3D12 \_ Разрешить \_ одновременный \_ флаг доступа неявно получаются из D3D12ного \_ состояния ресурса, \_ \_ общего для соответствующего состояния при первом доступе к GPU, включая универсальное \_ чтение, охватывающее любой сценарий чтения. Доступ к любому ресурсу в общем состоянии можно получить, как если бы он находился в одном состоянии с

<dl> 1 флаг записи или  
1 или несколько флагов чтения  
</dl>

Ресурсы можно повысить на основе общего состояния, основанного на следующей таблице.



| Флаг состояния                    | Буферы и текстуры Simultaneous-Access                             | Текстуры без одновременного доступа                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| ВЕРШИНный \_ и \_ Постоянный \_ буфер | Да                                          | Нет                                   |
| буфер ИНДЕКСов \_                 | Да                                          | Нет                                   |
| \_целевой объект прорисовки                | Да                                          | Нет                                   |
| неупорядоченный \_ доступ             | Да                                          | Нет                                   |
| \_запись глубины                  | Нет<sup>\*</sup>                              | Нет                                   |
| чтение с ГЛУБИНой \_                   | Нет<sup>\*</sup>                              | Нет                                   |
| \_ \_ ресурс шейдера, не являющегося пиксельным \_  | Да                                          | Да                                  |
| \_ресурс шейдера \_ пикселей       | Да                                          | Да                                  |
| \_потоковая передача                   | Да                                          | Нет                                   |
| непрямое \_ аргумент            | Да                                          | Нет                                   |
| Копировать \_ конечный                    | Да                                          | Да                                  |
| Копировать \_ источник                  | Да                                          | Да                                  |
| Разрешить \_ конечный                 | Да                                          | Нет                                   |
| Разрешить \_ источник               | Да                                          | Нет                                   |
| ЗАТЕНЕНИЯ                   | Да                                          | Нет                                   |



 

<sup>\*</sup>Ресурсы шаблона глубины должны быть текстурами, не поддерживающими одновременный доступ, и поэтому никогда не могут быть косвенно выдвинуты.

Когда этот доступ происходит, повышение действует как неявный барьер ресурсов. Для последующих обращений к ресурсам при необходимости потребуется изменить состояние ресурса. Обратите внимание, что продвижение от одного уровня чтения до нескольких состояний чтения допустимо, но это не так для записи состояния.  
Например, если ресурс в общем состоянии повышен до \_ ресурса шейдера пикселей \_ в вызове Draw, его все равно можно повысить до NON_PIXEL \_ ресурса шейдера \_ | \_Ресурс шейдера пикселей \_ в другом вызове Draw. Однако, если он используется в операции записи, такой как назначение копирования, барьер перехода состояния ресурса из Объединенных состояний чтения повышенного уровня, здесь NON_PIXEL \_ ресурс шейдера \_ | \_Требуется ресурс шейдера пикселей \_ для копирования \_ dest.  
Аналогично, при повышении уровня общего \_ назначения для копирования конечного объекта барьер по-прежнему требуется для перехода от \_ приемника копирования к \_ ЦЕЛЕВому объекту рендеринга.

Обратите внимание, что распространенное повышение состояния является "свободным", так что GPU не требуется для выполнения каких-либо ожиданий синхронизации. Продвижение представляет тот факт, что ресурсы в общем состоянии не должны требовать дополнительного отслеживания GPU или драйверов для поддержки определенных операций доступа.

### <a name="state-decay-to-common"></a>Decay состояния для общего

Зеркальная сторона повышения общего состояния Decay обратно в D3D12ное \_ \_ состояние ресурса \_ . Ресурсы, соответствующие определенным требованиям, считаются без отслеживания состояния и фактически возвращаются в общее состояние, когда GPU завершает выполнение операции [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) . Decay не происходит между списками команд, выполняемых вместе в одном вызове **ексекутекоммандлистс** .

Следующие ресурсы будут Decay при завершении операции [**ексекутекоммандлистс**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) на GPU:

-   Ресурсы, к которым осуществляется доступ в очереди копирования, *или*
-   Буферные ресурсы в любом типе очереди *или*
-   Ресурсы текстуры в любом типе очереди, для которых установлен \_ флаг ресурса D3D12 \_ \_ Разрешить \_ одновременный \_ доступ, *или*
-   Любой ресурс неявным образом повышается до состояния только для чтения.

Как и при распространении состояния, Decay предоставляется бесплатно в том случае, если дополнительная синхронизация не требуется. Сочетание распространенного повышения состояния и Decay может помочь устранить множество ненужных переходов [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) . В некоторых случаях это может привести к значительному улучшению производительности.

Буферы и Simultaneous-Access ресурсы будут Decay к общему состоянию независимо от того, были ли они явно перенесены с помощью барьеров ресурсов или неявно повышены.

### <a name="performance-implications"></a>Влияние на производительность

При записи явных [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) переходов для ресурсов в общем состоянии необходимо использовать \_ общее состояние ресурса D3D12 или любое переопределяющее \_ \_ состояние как значение *бефорестате* в \_ \_ \_ структуре барьера перехода ресурсов D3D12. Это обеспечивает традиционное управление состоянием, которое игнорирует автоматические Decay буферов и текстуры с одновременным доступом. Это может быть нежелательно, так как предотвращение **ресаурцебарриер** вызовов с ресурсами, которые находятся в общем состоянии, может значительно повысить производительность. Барьеры ресурсов могут быть дорогостоящими. Они предназначены для принудительного сброса кэша, изменения макета памяти и другие операции синхронизации, которые могут не потребоваться для ресурсов, которые уже находятся в общем состоянии. Список команд, использующий барьер ресурсов из нераспространенного состояния в другое необычное состояние для ресурса, находящегося в общем состоянии, может привести к ненужным издержкам.

Кроме того, следует избегать явного перехода [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) в D3D12ное \_ состояние ресурса, \_ \_ если это не обязательно (например, следующий доступ находится в очереди команд копирования, для которой требуется, чтобы ресурсы начали в общем состоянии). Чрезмерное число переходов к общему состоянию может значительно замедлить производительность GPU.

В целом, постарайтесь полагаться на распространенное повышение состояния и Decay каждый раз, когда его семантика позволяет избежать выполнения вызовов [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .

## <a name="split-barriers"></a>Разделите барьеры

Барьер переключения ресурсов с \_ \_ флагом запуска D3D12а барьера ресурсов \_ \_ \_ начинает разбивать барьер, а барьер перехода считается ожидающим. Пока барьер находится в состоянии ожидания, ресурс (подкласс) не может быть прочитан или записан с помощью GPU. Единственный допустимый барьер переходов, который можно применить к ресурсу (подзадаче) с ожидающим барьером, — это один из состояний *до* и *после* , а также флаг D3D12а \_ \_ барьера ресурсов \_ \_ \_ , который барьер завершает ожидание ожидающего перехода.

Разделите барьеры предоставляют подсказки для GPU, которые ресурс в состоянии *а* затем будет использоваться в состоянии *б* позже. Это дает GPU возможность оптимизировать рабочую нагрузку перехода, что может привести к сокращению или устранению ожидания выполнения. При выдаче конечного барьера гарантируется, что все операции перехода GPU завершаются до перехода к следующей команде.

С помощью раздельных барьеров можно повысить производительность, особенно в сценариях с несколькими модулями или при том, что ресурсы, доступные для чтения и записи, распределены по всему одному или нескольким спискам команд.

## <a name="resource-barrier-example-scenario"></a>Пример сценария барьера ресурсов

В следующих фрагментах кода показано использование метода [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) в примере многопоточности.

Создание представления трафарета глубины с переходом в состояние, доступное для записи.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Создание представления буфера вершин, сначала изменение его из общего состояния на назначение, а затем из места назначения в общее доступное для чтения состояние.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Создание представления буфера индексов, сначала изменение его из общего состояния на назначение, а затем из места назначения в общее доступное для чтения состояние.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Создание текстур и представлений ресурсов шейдера. Текстура изменяется от общего состояния к назначению, а затем от назначения к ресурсу шейдера пикселей.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Начало кадра; Он не только использует [**ресаурцебарриер**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) для указания того, что в качестве целевого объекта рендеринга используется буфер обмена, но также инициализируется ресурс кадра (который вызывает **ресаурцебарриер** в буфере трафарета глубины).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Завершение кадра с указанием заднего буфера, который теперь используется для представления.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



Инициализация ресурса фрейма, вызываемого при начале кадра, переводит буфер трафарета глубины в доступный для записи.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Барьеры направляются в середину фрейма, переходя к теневой карте с возможностью чтения.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Метод Finish вызывается, когда кадр завершается, переключается на теневую карту в общее состояние.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Пример повышения общего состояния и Decay

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Пример разделенных барьеров

В следующем примере показано использование барьера разделения для уменьшения количества ожиданий конвейера. Следующий код не использует барьеры разделения:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

В следующем коде используются барьеры разделения:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Связанные темы

[Учебные видеоматериалы по DirectX для расширенного обучения: барьеры ресурсов и отслеживание состояния](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Синхронизация с несколькими движками](./user-mode-heap-synchronization.md)

[Отправка работы в Direct3D 12](command-queues-and-command-lists.md)

[Взгляните на барьеры состояния ресурсов D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)


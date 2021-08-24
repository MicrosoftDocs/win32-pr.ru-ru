---
title: Системы с несколькими адаптерами
description: Описание поддержки в Direct3D 12 для систем с несколькими установленными адаптерами, охватывающие сценарии, в которых приложение явно предназначено для нескольких адаптеров GPU, и сценарии, в которых драйверы неявно используют несколько адаптеров GPU от имени приложения.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: e76c5c1295dab8858ff04830030efb479fe3ae8a09bcdb37ff8c4820f4fd08c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728823"
---
# <a name="multi-adapter-systems"></a>Системы с несколькими адаптерами

Описание поддержки в Direct3D 12 для систем с несколькими установленными адаптерами, охватывающие сценарии, в которых приложение явно предназначено для нескольких адаптеров GPU, и сценарии, в которых драйверы неявно используют несколько адаптеров GPU от имени приложения.

## <a name="multi-adapter-overview"></a>Общие сведения о нескольких адаптерах

Адаптер GPU может быть любым адаптером (графическим или вычислительным, дискретным или интегрированным) от любого производителя, который поддерживает Direct3D 12.

На несколько адаптеров ссылаются как на *узлы*. Ряд элементов, например очередей, применяется к каждому узлу, поэтому при наличии двух узлов будут использоваться две трехмерные очереди по умолчанию. Другие элементы, такие как состояние конвейера и сигнатуры корня и команды, могут ссылаться на один или несколько узлов, как показано на схеме.

![очереди применяются к каждому графическому адаптеру.](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Совместное использование куч в адаптерах

См. раздел [Общие кучи](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>API-интерфейсы нескольких адаптеров и маски узлов

Как и в предыдущих API-интерфейсах Direct3D, каждый набор связанных адаптеров перечисляется как один объект [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) . Все выходные данные, присоединенные к любому адаптеру в связи, перечисляются как прикрепленные к отдельному объекту **IDXGIAdapter3** .

Приложение может определить число физических адаптеров, связанных с данным устройством, вызвав [**ID3D12Device:: жетнодекаунт**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Многие API-интерфейсы в Direct3D 12 принимают *маску узла* (битовую маску), которая указывает набор узлов, к которым относится этот вызов API. Каждый узел содержит индекс, начинающийся с нуля. Но в маске узла нуль преобразуется в бит 1; 1 преобразуется в бит 2; и т. д.

### <a name="single-nodes"></a>Отдельные узлы

При вызове следующих API (один узел) в приложении указывается единственный узел, с которым будет связан вызов API. В большинстве случаев это определяется маской узла. Каждый бит маски соответствует одному узлу. Для всех интерфейсов API, описанных в этом разделе, необходимо установить ровно один бит в маске узла.

-   [**D3D12 \_ \_Очередь команд \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : содержит элемент *нодемаск* .
-   [**Креатекоммандкуеуе**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : создает очередь из структуры в [**\_ \_ очереди \_ команд D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**Креатекоммандлист**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : принимает параметр *нодемаск* .
-   [**D3D12 \_ В \_ КУЧЕ \_ дескрипторов DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : имеет элемент *нодемаск* .
-   [**Креатедескрипторхеап**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : создает кучу дескрипторов в структуре [**\_ \_ \_ DESC дескриптора D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) .
-   [**D3D12 \_ В \_ КУЧЕ запросов \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : имеется элемент *нодемаск* .
-   [**Креатекуерихеап**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : создает кучу запросов из структуры [**\_ \_ кучи \_ запросов D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Несколько узлов

При вызове следующих API (несколько узлов) в приложении указывается набор узлов, с которыми будет связан вызов API. Сходство узлов указывается как маска узла, возможно, с несколькими наборами битов. Если приложение передает значение 0 для этой битовой маски, драйвер Direct3D 12 преобразует его в битовую маску 1 (указывающую, что объект связан с узлом 0).

-   [**D3D12 \_ \_ \_ \_ Уровень совместного использования**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) узлов: определяет поддержку совместного использования между узлами.
-   [**D3D12 \_ ФУНКЦИИ \_ \_ D3D12 данных \_ Параметры**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : структура, ссылающаяся на [**\_ \_ \_ \_ уровень совместного использования D3D12ных**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)узлов.
-   [**D3D12 \_ \_ \_ Архитектура данных компонента**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : содержит элемент *нодеиндекс* .
-   [**D3D12 \_ \_Состояние графического конвейера \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : имеет элемент *нодемаск* .
-   [**Креатеграфикспипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : создает объект состояния графического конвейера из структуры [**описания \_ \_ состояния графического \_ \_ конвейера D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .
-   [**D3D12 \_ ВЫЧИСЛЕНие \_ \_ состояния \_ конвейера вычислений**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : имеет элемент *нодемаск* .
-   [**Креатекомпутепипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : создает объект состояния вычислений конвейера из структуры [**описания \_ \_ \_ состояния \_ конвейера вычислений D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .
-   [**Креатерутсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature): принимает параметр *нодемаск* .
-   [**D3D12 \_ \_ \_ DESC сигнатуры команды**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc): содержит элемент *нодемаск* .
-   [**Креатекоммандсигнатуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : создает объект сигнатуры команды на основе [**структуры \_ \_ сигнатуры \_ команды D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) .

### <a name="resource-creation-apis"></a>API-интерфейсы для создания ресурсов

Следующие API ссылаются на маски узлов.

-   [**D3D12 \_ \_Свойства кучи**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : содержит члены *креатионнодемаск* и *висибленодемаск* .
-   [**Жетресаурцеаллокатионинфо**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : имеет параметр *висиблемаск* .
-   [**Жеткустомхеаппропертиес**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : имеет параметр *нодемаск* .

При создании зарезервированного ресурса не указывается индекс или маска узла. Зарезервированный ресурс можно сопоставить с кучей на любом узле (после правил общего доступа между узлами).

Метод [**макересидент**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) работает внутренне с очередями адаптеров. в приложении нет необходимости указывать что-либо для этого.

При вызове следующих API [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) приложению не нужно указывать набор узлов, с которыми будет связан вызов API, поскольку вызов API применяется ко всем узлам.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**Опеншаредхандле**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : с *ограждением* в качестве параметра. С помощью *ресурса* или *кучи* в качестве параметров этот метод не принимает узлы в качестве параметров, так как маски узлов наследуются от ранее созданных объектов.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Связанные темы

[Руководство по программированию для Direct3D 12](directx-12-programming-guide.md)
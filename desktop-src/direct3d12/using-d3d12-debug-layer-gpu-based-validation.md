---
title: Проверка на основе GPU и уровень отладки Direct3D 12
description: В этом разделе описывается, как лучше использовать уровень отладки Direct3D 12. Проверка на основе GPU (ГБВ) включает сценарии проверки на временной шкале GPU, которые невозможны во время вызовов API в ЦП.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 63e1ebbe34bbb94fbdf52b374b10283100e3bfa432338521a9807497b236d868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952744"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Проверка на основе GPU и уровень отладки Direct3D 12

В этом разделе описывается, как лучше использовать уровень отладки Direct3D 12. Проверка на основе GPU (ГБВ) включает сценарии проверки на временной шкале GPU, которые невозможны во время вызовов API в ЦП. гбв доступен, начиная с графических средств для обновления годовщины Windows 10.

## <a name="purpose-of-gpu-based-validation"></a>Назначение проверки на основе GPU

Проверка на основе GPU помогает обнаруживать следующие ошибки:

- Использование неинициализированных или несовместимых дескрипторов в шейдере.
- Использование дескрипторов, ссылающихся на удаленные ресурсы в шейдере.
- Проверка состояния повышенных ресурсов и Decay состояния ресурсов.
- Индексация за пределами кучи дескрипторов в шейдере.
- Доступ шейдера к ресурсам в несовместимом состоянии.
- Использование неинициализированных или несовместимых проб в шейдере.

ГБВ работает путем создания исправленных шейдеров, которые содержат проверку, добавленную непосредственно в шейдер. Обновленные шейдеры проверяют корневые аргументы и ресурсы, к которым обращаются во время выполнения шейдера, и сообщают об ошибках в буфер журнала. ГБВ также внедряет дополнительные операции и передает вызовы в списки команд приложения для проверки и отслеживания изменений в состоянии ресурсов, накладываемых списком команд на временной шкале GPU.

Поскольку для ГБВ требуется возможность выполнения шейдеров, списки команд копирования можно эмулировать с помощью списка команд вычислений. Это потенциально может изменить то, как оборудование выполняет копирование, хотя конечный результат не должен изменяться. Приложение по-прежнему будет воспринимать эти списки команд COPY, а отладочный слой будет проверять их.

## <a name="turning-on-gpu-based-validation"></a>Включение проверки на основе GPU

ГБВ можно принудительно использовать с помощью панели управления DirectX (ДКСКПЛ), переведя на уровень отладки Direct3D 12 и дополнительно вызывая проверку на основе GPU (Новая вкладка на панели управления). После включения ГБВ будет оставаться включенным до выпуска устройства Direct3D 12. Кроме того, ГБВ можно включить программно перед созданием устройства Direct3D 12:

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a>Рекомендуемый способ использования

Как правило, в большинстве случаев следует запускать код с включенным уровнем отладки. Однако ГБВ может замедлить выполнение большого числа операций. Разработчики могут рассмотреть возможность включения ГБВ с меньшими наборами данных (например, демонстрацией подсистемы или малыми уровнями игры с меньшим количеством PSO и ресурсов) или на ранних этапах работы приложения, чтобы снизить проблемы с производительностью. С большим содержимым рассмотрите возможность включения ГБВ на одном или двух тестовых компьютерах в ходе ночных тестов.

## <a name="debug-output"></a>Выходные данные отладки

ГБВ создает выходные данные отладки после того, как вызов [**ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) завершает выполнение на GPU. Так как это происходит на временной шкале GPU, выходные данные отладки могут быть асинхронными с другой проверкой временной шкалы ЦП. Для синхронизации выходных данных отладки разработчикам приложений может потребоваться ввести собственные ожидания выполнения.

ГБВ Output определяет, в каком месте шейдера произошла ошибка, а также текущее число операций рисования/диспетчеризации и идентификаторы связанных объектов (например, список команд, очередь, PSO и т. д.).

## <a name="example-debug-message"></a>Пример сообщения об отладке

Следующее сообщение об ошибке указывает, что доступ к ресурсу с именем "основной цветовой буфер" был получен в шейдере в виде ресурса шейдера, но он был в неупорядоченном состоянии при выполнении шейдера GPU. Также предоставляются дополнительные сведения, такие как расположение в источнике шейдера, имя списка команд и число штрихов (рисование индекса) и имена связанных объектов интерфейсов D3D.

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a>API слоя отладки

Чтобы включить слой отладки, вызовите [**енабледебуглайер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Чтобы включить проверку на основе GPU, вызовите [**сетенаблегпубаседвалидатион**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)и обратитесь к методам следующих интерфейсов:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

См. следующие перечисления и структуры:

- [**\_ \_ \_ \_ Тип параметра списка команд отладки \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**\_ \_ \_ Тип параметра устройства отладки \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**\_ \_ \_ \_ \_ \_ Флаги создания состояния КОНВЕЙЕРа проверки на основе GPU \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**\_ \_ \_ \_ Режим исправления шейдера проверки подлинности D3D12 на основе GPU \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**\_ \_ Список команд отладки \_ D3D12 \_ \_ \_ Параметры проверки на основе GPU \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**\_ \_ \_ \_ Параметры проверки на основе GPU \_ для устройства отладки D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Связанные темы

* [Основные сведения о слое отладки Direct3D 12](understanding-the-d3d12-debug-layer.md)

---
title: Проверка на основе GPU и уровень отладки Direct3D 12
description: В этом разделе описывается, как лучше использовать уровень отладки Direct3D 12. Проверка на основе GPU (ГБВ) включает сценарии проверки на временной шкале GPU, которые невозможны во время вызовов API в ЦП.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549019"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="d1bcc-104">Проверка на основе GPU и уровень отладки Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d1bcc-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="d1bcc-105">В этом разделе описывается, как лучше использовать уровень отладки Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="d1bcc-106">Проверка на основе GPU (ГБВ) включает сценарии проверки на временной шкале GPU, которые невозможны во время вызовов API в ЦП.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="d1bcc-107">ГБВ доступен начиная с годовщины обработки графики для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="d1bcc-108">Назначение проверки на основе GPU</span><span class="sxs-lookup"><span data-stu-id="d1bcc-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="d1bcc-109">Проверка на основе GPU помогает обнаруживать следующие ошибки:</span><span class="sxs-lookup"><span data-stu-id="d1bcc-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="d1bcc-110">Использование неинициализированных или несовместимых дескрипторов в шейдере.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="d1bcc-111">Использование дескрипторов, ссылающихся на удаленные ресурсы в шейдере.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="d1bcc-112">Проверка состояния повышенных ресурсов и Decay состояния ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="d1bcc-113">Индексация за пределами кучи дескрипторов в шейдере.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="d1bcc-114">Доступ шейдера к ресурсам в несовместимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="d1bcc-115">Использование неинициализированных или несовместимых проб в шейдере.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="d1bcc-116">ГБВ работает путем создания исправленных шейдеров, которые содержат проверку, добавленную непосредственно в шейдер.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="d1bcc-117">Обновленные шейдеры проверяют корневые аргументы и ресурсы, к которым обращаются во время выполнения шейдера, и сообщают об ошибках в буфер журнала.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="d1bcc-118">ГБВ также внедряет дополнительные операции и передает вызовы в списки команд приложения для проверки и отслеживания изменений в состоянии ресурсов, накладываемых списком команд на временной шкале GPU.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="d1bcc-119">Поскольку для ГБВ требуется возможность выполнения шейдеров, списки команд копирования можно эмулировать с помощью списка команд вычислений.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="d1bcc-120">Это потенциально может изменить то, как оборудование выполняет копирование, хотя конечный результат не должен изменяться.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="d1bcc-121">Приложение по-прежнему будет воспринимать эти списки команд COPY, а отладочный слой будет проверять их.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="d1bcc-122">Включение проверки на основе GPU</span><span class="sxs-lookup"><span data-stu-id="d1bcc-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="d1bcc-123">ГБВ можно принудительно использовать с помощью панели управления DirectX (ДКСКПЛ), переведя на уровень отладки Direct3D 12 и дополнительно вызывая проверку на основе GPU (Новая вкладка на панели управления).</span><span class="sxs-lookup"><span data-stu-id="d1bcc-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="d1bcc-124">После включения ГБВ будет оставаться включенным до выпуска устройства Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="d1bcc-125">Кроме того, ГБВ можно включить программно перед созданием устройства Direct3D 12:</span><span class="sxs-lookup"><span data-stu-id="d1bcc-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

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

## <a name="recommended-usage"></a><span data-ttu-id="d1bcc-126">Рекомендуемый способ использования</span><span class="sxs-lookup"><span data-stu-id="d1bcc-126">Recommended usage</span></span>

<span data-ttu-id="d1bcc-127">Как правило, в большинстве случаев следует запускать код с включенным уровнем отладки.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="d1bcc-128">Однако ГБВ может замедлить выполнение большого числа операций.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="d1bcc-129">Разработчики могут рассмотреть возможность включения ГБВ с меньшими наборами данных (например, демонстрацией подсистемы или малыми уровнями игры с меньшим количеством PSO и ресурсов) или на ранних этапах работы приложения, чтобы снизить проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="d1bcc-130">С большим содержимым рассмотрите возможность включения ГБВ на одном или двух тестовых компьютерах в ходе ночных тестов.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="d1bcc-131">Выходные данные отладки</span><span class="sxs-lookup"><span data-stu-id="d1bcc-131">Debug output</span></span>

<span data-ttu-id="d1bcc-132">ГБВ создает выходные данные отладки после того, как вызов [**ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) завершает выполнение на GPU.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="d1bcc-133">Так как это происходит на временной шкале GPU, выходные данные отладки могут быть асинхронными с другой проверкой временной шкалы ЦП.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="d1bcc-134">Для синхронизации выходных данных отладки разработчикам приложений может потребоваться ввести собственные ожидания выполнения.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="d1bcc-135">ГБВ Output определяет, в каком месте шейдера произошла ошибка, а также текущее число операций рисования/диспетчеризации и идентификаторы связанных объектов (например, список команд, очередь, PSO и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d1bcc-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="d1bcc-136">Пример сообщения об отладке</span><span class="sxs-lookup"><span data-stu-id="d1bcc-136">Example debug message</span></span>

<span data-ttu-id="d1bcc-137">Следующее сообщение об ошибке указывает, что доступ к ресурсу с именем "основной цветовой буфер" был получен в шейдере в виде ресурса шейдера, но он был в неупорядоченном состоянии при выполнении шейдера GPU.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="d1bcc-138">Также предоставляются дополнительные сведения, такие как расположение в источнике шейдера, имя списка команд и число штрихов (рисование индекса) и имена связанных объектов интерфейсов D3D.</span><span class="sxs-lookup"><span data-stu-id="d1bcc-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

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

## <a name="debug-layer-apis"></a><span data-ttu-id="d1bcc-139">API слоя отладки</span><span class="sxs-lookup"><span data-stu-id="d1bcc-139">Debug Layer APIs</span></span>

<span data-ttu-id="d1bcc-140">Чтобы включить слой отладки, вызовите [**енабледебуглайер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span><span class="sxs-lookup"><span data-stu-id="d1bcc-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="d1bcc-141">Чтобы включить проверку на основе GPU, вызовите [**сетенаблегпубаседвалидатион**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)и обратитесь к методам следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="d1bcc-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="d1bcc-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="d1bcc-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="d1bcc-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="d1bcc-145">См. следующие перечисления и структуры:</span><span class="sxs-lookup"><span data-stu-id="d1bcc-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="d1bcc-146">**\_ \_ \_ \_ Тип параметра списка команд отладки \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="d1bcc-147">**\_ \_ \_ Тип параметра устройства отладки \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="d1bcc-148">**\_ \_ \_ \_ \_ \_ Флаги создания состояния КОНВЕЙЕРа проверки на основе GPU \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="d1bcc-149">**\_ \_ \_ \_ Режим исправления шейдера проверки подлинности D3D12 на основе GPU \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="d1bcc-150">**\_ \_ Список команд отладки \_ D3D12 \_ \_ \_ Параметры проверки на основе GPU \_**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="d1bcc-151">**\_ \_ \_ \_ Параметры проверки на основе GPU \_ для устройства отладки D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="d1bcc-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="d1bcc-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d1bcc-152">Related topics</span></span>

* [<span data-ttu-id="d1bcc-153">Основные сведения о слое отладки Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d1bcc-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)

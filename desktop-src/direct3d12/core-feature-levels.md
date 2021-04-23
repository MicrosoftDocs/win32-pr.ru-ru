---
title: Уровень компонентов Direct3D 12 Core 1.0
description: Основной уровень компонентов 1,0 является подмножеством полного набора функций Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2020
ms.locfileid: "105719120"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="a3c82-103">Уровень компонентов Direct3D 12 Core 1.0</span><span class="sxs-lookup"><span data-stu-id="a3c82-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="a3c82-104">Основной уровень компонентов 1,0 является подмножеством полного набора функций Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="a3c82-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="a3c82-105">Уровень компонентов Core 1,0 может предоставляться категорией устройств, которые называются *устройствами только для вычислений*.</span><span class="sxs-lookup"><span data-stu-id="a3c82-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="a3c82-106">Общая модель драйвера для устройств, предназначенных только для вычислений, — это модель вычислений Microsoft COMPUTE Driver (МКДМ).</span><span class="sxs-lookup"><span data-stu-id="a3c82-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="a3c82-107">МКДМ — это масштабируемый одноранговый узел модели драйверов устройств Windows (WDDM), имеющий более широкую область.</span><span class="sxs-lookup"><span data-stu-id="a3c82-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="a3c82-108">Устройство, которое поддерживает *только* функции в базовом уровне, называется *основным устройством*.</span><span class="sxs-lookup"><span data-stu-id="a3c82-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c82-109">*Устройство только для вычислений*, устройство *мкдм*, *базовое устройство уровня функций* и *Основное устройство* означают одно и то же.</span><span class="sxs-lookup"><span data-stu-id="a3c82-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="a3c82-110">Для простоты мы предпочитаем *Основное устройство* .</span><span class="sxs-lookup"><span data-stu-id="a3c82-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="a3c82-111">Создание базового устройства</span><span class="sxs-lookup"><span data-stu-id="a3c82-111">Creating a Core device</span></span>

<span data-ttu-id="a3c82-112">Как правило, для создания устройства Direct3D 12 вызывается функция [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) и указывается минимальный уровень компонента.</span><span class="sxs-lookup"><span data-stu-id="a3c82-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="a3c82-113">Если указать уровень признаков от 9 до 12, то возвращенное устройство является устройством с богатыми возможностями, например традиционным графическим процессором (который поддерживает надмножество функций основного устройства).</span><span class="sxs-lookup"><span data-stu-id="a3c82-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="a3c82-114">Основное устройство никогда не возвращается для этого диапазона уровней функций.</span><span class="sxs-lookup"><span data-stu-id="a3c82-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="a3c82-115">С другой стороны, если указать основной уровень компонентов (например, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), то возвращаемое устройство может быть многофункциональным или базовым устройством.</span><span class="sxs-lookup"><span data-stu-id="a3c82-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="a3c82-116">Если указан `_CORE` уровень компонента, то уровень среды выполнения и отладки проверяет, что функции, используемые приложением, разрешены этим `_CORE` уровнем функций.</span><span class="sxs-lookup"><span data-stu-id="a3c82-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="a3c82-117">Этот набор функций определен далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a3c82-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="a3c82-118">Модель шейдера для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-118">Shader model for Core devices</span></span>

<span data-ttu-id="a3c82-119">Устройство ядра поддерживает модель шейдеров версии 5.0 +.</span><span class="sxs-lookup"><span data-stu-id="a3c82-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="a3c82-120">Среда выполнения выполняет преобразование моделей шейдера 5. x без ДКСИЛ в 6,0 ДКСИЛ.</span><span class="sxs-lookup"><span data-stu-id="a3c82-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="a3c82-121">Поэтому драйверу требуется только поддержка 6. x.</span><span class="sxs-lookup"><span data-stu-id="a3c82-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="a3c82-122">Модель управления ресурсами для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="a3c82-123">Поддерживаемые измерения ресурсов: только необработанные и структурированные буферы (без типизированных буферов, texture1d/2D и т. д.)</span><span class="sxs-lookup"><span data-stu-id="a3c82-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="a3c82-124">Нет поддержки зарезервированных (мозаичных) ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3c82-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="a3c82-125">Нет поддержки пользовательских куч</span><span class="sxs-lookup"><span data-stu-id="a3c82-125">No support for custom heaps</span></span>
- <span data-ttu-id="a3c82-126">Ни один из следующих флагов кучи не поддерживается:</span><span class="sxs-lookup"><span data-stu-id="a3c82-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="a3c82-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="a3c82-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="a3c82-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="a3c82-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="a3c82-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="a3c82-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="a3c82-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Обратите внимание, что требуются атомарные шейдеры, этот флаг предназначен для другого компонента, атомарных операций с разными адаптерами).</span><span class="sxs-lookup"><span data-stu-id="a3c82-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="a3c82-131">Модель привязки ресурсов для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="a3c82-132">Поддержка только для уровня привязки ресурсов 1</span><span class="sxs-lookup"><span data-stu-id="a3c82-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="a3c82-133">Исключения:</span><span class="sxs-lookup"><span data-stu-id="a3c82-133">Exceptions:</span></span>
  - <span data-ttu-id="a3c82-134">Нет поддержки для образцов текстуры</span><span class="sxs-lookup"><span data-stu-id="a3c82-134">No support for texture samplers</span></span>
  - <span data-ttu-id="a3c82-135">Поддержка 64 Уавс, например, уровень функции 11.1 + (в отличие от 8).</span><span class="sxs-lookup"><span data-stu-id="a3c82-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="a3c82-136">Реализациям не требуется реализовывать проверку границ для доступа шейдера к ресурсам через дескрипторы, доступ к которым вызывает неопределенное поведение.</span><span class="sxs-lookup"><span data-stu-id="a3c82-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="a3c82-137">В качестве побочным эффектом флаг диапазона дескрипторов D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS в корневых сигнатурах не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a3c82-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="a3c82-138">Дескрипторы UAV и CBV могут быть сделаны только для ресурсов из куч по умолчанию (без куч отправки и реадбакк).</span><span class="sxs-lookup"><span data-stu-id="a3c82-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="a3c82-139">Это заставляет приложение выполнять копирование для получения данных между ЦП<->GPU.</span><span class="sxs-lookup"><span data-stu-id="a3c82-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="a3c82-140">Несмотря на то, что это самый низкий уровень возможностей привязки, некоторые функции, которые необходимо выполнить даже на этом уровне, все еще стоит вызывать:</span><span class="sxs-lookup"><span data-stu-id="a3c82-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="a3c82-141">Кучи дескрипторов можно обновлять после записи списков команд (см. D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE в спецификации привязки ресурсов).</span><span class="sxs-lookup"><span data-stu-id="a3c82-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="a3c82-142">Корневые дескрипторы — это, по сути, ГПУВА указатели</span><span class="sxs-lookup"><span data-stu-id="a3c82-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="a3c82-143">Несмотря на отсутствие поддержки ММУ/ва, буфер VAs, используемый в корневых дескрипторах, может эмулироваться реализациями путем исправления адресов.</span><span class="sxs-lookup"><span data-stu-id="a3c82-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="a3c82-144">Ограничения структурированного буфера</span><span class="sxs-lookup"><span data-stu-id="a3c82-144">Structured buffer restrictions</span></span>

<span data-ttu-id="a3c82-145">Структурированные буферы должны иметь базовый адрес размером 4 байта, а шаг должен быть 2 или кратным 4.</span><span class="sxs-lookup"><span data-stu-id="a3c82-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="a3c82-146">Случай для шага 2 — для приложений с 16-разрядными данными, особенно учитывая, что в D3D_FEATURE_LEVEL_1_0_CORE не поддерживается типизированные буферы.</span><span class="sxs-lookup"><span data-stu-id="a3c82-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="a3c82-147">Шаг, указанный в дескрипторах, должен соответствовать STRIDE, указанному в HLSL.</span><span class="sxs-lookup"><span data-stu-id="a3c82-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="a3c82-148">Поддержка очереди команд для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-148">Command queue support for Core devices</span></span>

<span data-ttu-id="a3c82-149">Вычислять и копировать только очереди (без 3D, видео и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a3c82-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="a3c82-150">Поддержка шейдера для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-150">Shader support for Core devices</span></span>

<span data-ttu-id="a3c82-151">Только для шейдеров вычислений, без графических шейдеров (вершин, шейдеры пикселей и т. д.) и любых связанных функций, таких как целевые объекты рендеринга, цепочки буфера обмена, входной ассемблер.</span><span class="sxs-lookup"><span data-stu-id="a3c82-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="a3c82-152">Арифметическая точность</span><span class="sxs-lookup"><span data-stu-id="a3c82-152">Arithmetic precision</span></span>

<span data-ttu-id="a3c82-153">Базовые устройства не должны поддерживать денорму для 16 разрядных операций с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="a3c82-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="a3c82-154">Поддерживаемые API для основных устройств</span><span class="sxs-lookup"><span data-stu-id="a3c82-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="a3c82-155">*Приведенный* ниже список представляет поддерживаемое подмножество полного прикладного программного интерфейса (API, которые *не* поддерживаются на уровне компонента Core 1,0).</span><span class="sxs-lookup"><span data-stu-id="a3c82-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="a3c82-156">Методы ID3D12Device</span><span class="sxs-lookup"><span data-stu-id="a3c82-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="a3c82-157">ID3D12Device:: Чеккфеатуресуппорт</span><span class="sxs-lookup"><span data-stu-id="a3c82-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="a3c82-158">ID3D12Device:: Копидескрипторс</span><span class="sxs-lookup"><span data-stu-id="a3c82-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="a3c82-159">ID3D12Device:: Копидескрипторссимпле</span><span class="sxs-lookup"><span data-stu-id="a3c82-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="a3c82-160">ID3D12Device:: Креатекоммандаллокатор</span><span class="sxs-lookup"><span data-stu-id="a3c82-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="a3c82-161">ID3D12Device:: Креатекоммандлист</span><span class="sxs-lookup"><span data-stu-id="a3c82-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="a3c82-162">ID3D12Device:: Креатекоммандкуеуе</span><span class="sxs-lookup"><span data-stu-id="a3c82-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="a3c82-163">ID3D12Device:: Креатекоммандсигнатуре</span><span class="sxs-lookup"><span data-stu-id="a3c82-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="a3c82-164">ID3D12Device:: Креатекоммиттедресаурце</span><span class="sxs-lookup"><span data-stu-id="a3c82-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="a3c82-165">ID3D12Device:: Креатекомпутепипелинестате</span><span class="sxs-lookup"><span data-stu-id="a3c82-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="a3c82-166">ID3D12Device:: Креатеконстантбуффервиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="a3c82-167">ID3D12Device:: Креатедескрипторхеап</span><span class="sxs-lookup"><span data-stu-id="a3c82-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="a3c82-168">ID3D12Device:: Креатефенце</span><span class="sxs-lookup"><span data-stu-id="a3c82-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="a3c82-169">ID3D12Device:: CreateHeap</span><span class="sxs-lookup"><span data-stu-id="a3c82-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="a3c82-170">ID3D12Device:: Креатеплацедресаурце</span><span class="sxs-lookup"><span data-stu-id="a3c82-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="a3c82-171">ID3D12Device:: Креатекуерихеап</span><span class="sxs-lookup"><span data-stu-id="a3c82-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="a3c82-172">ID3D12Device:: Креатерутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="a3c82-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="a3c82-173">ID3D12Device:: Креатешадерресаурцевиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="a3c82-174">ID3D12Device:: Креатешаредхандле</span><span class="sxs-lookup"><span data-stu-id="a3c82-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="a3c82-175">ID3D12Device:: Креатеунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="a3c82-176">ID3D12Device:: вытеснение</span><span class="sxs-lookup"><span data-stu-id="a3c82-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="a3c82-177">ID3D12Device:: Жетадаптерлуид</span><span class="sxs-lookup"><span data-stu-id="a3c82-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="a3c82-178">ID3D12Device:: GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="a3c82-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="a3c82-179">ID3D12Device:: Жеткустомхеаппропертиес</span><span class="sxs-lookup"><span data-stu-id="a3c82-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="a3c82-180">ID3D12Device:: Жетдескрипторхандлеинкрементсизе</span><span class="sxs-lookup"><span data-stu-id="a3c82-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="a3c82-181">ID3D12Device:: Жетдевицеремоведреасон</span><span class="sxs-lookup"><span data-stu-id="a3c82-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="a3c82-182">ID3D12Device:: Жетнодекаунт</span><span class="sxs-lookup"><span data-stu-id="a3c82-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="a3c82-183">ID3D12Device:: Жетресаурцеаллокатионинфо</span><span class="sxs-lookup"><span data-stu-id="a3c82-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="a3c82-184">ID3D12Device:: Макересидент</span><span class="sxs-lookup"><span data-stu-id="a3c82-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="a3c82-185">ID3D12Device:: Опеншаредхандле</span><span class="sxs-lookup"><span data-stu-id="a3c82-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="a3c82-186">ID3D12Device:: Опеншаредхандлебинаме</span><span class="sxs-lookup"><span data-stu-id="a3c82-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="a3c82-187">ID3D12Device:: Сетстаблеповерстате</span><span class="sxs-lookup"><span data-stu-id="a3c82-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="a3c82-188">Методы ID3D12Device1</span><span class="sxs-lookup"><span data-stu-id="a3c82-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="a3c82-189">ID3D12Device1:: Креатепипелинелибрари</span><span class="sxs-lookup"><span data-stu-id="a3c82-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="a3c82-190">ID3D12Device1:: Сетевентонмултиплефенцекомплетион</span><span class="sxs-lookup"><span data-stu-id="a3c82-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="a3c82-191">ID3D12Device1:: Сетресиденцисетевентонмултиплефенцекомплетионприорити</span><span class="sxs-lookup"><span data-stu-id="a3c82-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="a3c82-192">Методы ID3D12Device2</span><span class="sxs-lookup"><span data-stu-id="a3c82-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="a3c82-193">ID3D12Device2:: Креатепипелинестате</span><span class="sxs-lookup"><span data-stu-id="a3c82-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="a3c82-194">Методы ID3D12Device3</span><span class="sxs-lookup"><span data-stu-id="a3c82-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="a3c82-195">ID3D12Device3:: Опенексистингхеапфромаддресс</span><span class="sxs-lookup"><span data-stu-id="a3c82-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="a3c82-196">[ID3D12Device3:: Опенексистингхеапфромфилемаппинг](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="a3c82-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="a3c82-197">ID3D12Device3:: Енкуеуемакересидент</span><span class="sxs-lookup"><span data-stu-id="a3c82-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="a3c82-198">Методы ID3D12Device4</span><span class="sxs-lookup"><span data-stu-id="a3c82-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="a3c82-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="a3c82-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="a3c82-200">Методы ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="a3c82-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="a3c82-201">ID3D12Device5:: Креатеметакомманд</span><span class="sxs-lookup"><span data-stu-id="a3c82-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="a3c82-202">ID3D12Device5:: Креатестатеобжект</span><span class="sxs-lookup"><span data-stu-id="a3c82-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="a3c82-203">ID3D12Device5:: Енумератеметакоммандпараметерс</span><span class="sxs-lookup"><span data-stu-id="a3c82-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="a3c82-204">ID3D12Device5:: Енумератеметакоммандс</span><span class="sxs-lookup"><span data-stu-id="a3c82-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="a3c82-205">ID3D12Device5:: Ремоведевице</span><span class="sxs-lookup"><span data-stu-id="a3c82-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="a3c82-206">Методы ID3D12CommandQueue</span><span class="sxs-lookup"><span data-stu-id="a3c82-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="a3c82-207">ID3D12CommandQueue:: Бегиневент</span><span class="sxs-lookup"><span data-stu-id="a3c82-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="a3c82-208">ID3D12CommandQueue:: Ендевент</span><span class="sxs-lookup"><span data-stu-id="a3c82-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="a3c82-209">ID3D12CommandQueue:: Ексекутекоммандлистс</span><span class="sxs-lookup"><span data-stu-id="a3c82-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="a3c82-210">ID3D12CommandQueue:: Жетклокккалибратион</span><span class="sxs-lookup"><span data-stu-id="a3c82-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="a3c82-211">ID3D12CommandQueue:: DESC</span><span class="sxs-lookup"><span data-stu-id="a3c82-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="a3c82-212">ID3D12CommandQueue:: Жеттиместампфрекуенци</span><span class="sxs-lookup"><span data-stu-id="a3c82-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="a3c82-213">ID3D12CommandQueue:: SetMarker</span><span class="sxs-lookup"><span data-stu-id="a3c82-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="a3c82-214">ID3D12CommandQueue:: сигнал</span><span class="sxs-lookup"><span data-stu-id="a3c82-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="a3c82-215">ID3D12CommandQueue:: wait</span><span class="sxs-lookup"><span data-stu-id="a3c82-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="a3c82-216">Методы ID3D12CommandList</span><span class="sxs-lookup"><span data-stu-id="a3c82-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="a3c82-217">ID3D12CommandList:: GetType</span><span class="sxs-lookup"><span data-stu-id="a3c82-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="a3c82-218">Методы ID3D12GraphicsCommandList</span><span class="sxs-lookup"><span data-stu-id="a3c82-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="a3c82-219">ID3D12GraphicsCommandList:: Бегиневент</span><span class="sxs-lookup"><span data-stu-id="a3c82-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="a3c82-220">ID3D12GraphicsCommandList:: Бегинкуери</span><span class="sxs-lookup"><span data-stu-id="a3c82-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="a3c82-221">ID3D12GraphicsCommandList:: Клеарстате</span><span class="sxs-lookup"><span data-stu-id="a3c82-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="a3c82-222">ID3D12GraphicsCommandList:: Клеарунордередакцессвиевфлоат</span><span class="sxs-lookup"><span data-stu-id="a3c82-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="a3c82-223">ID3D12GraphicsCommandList:: Клеарунордередакцессвиевуинт</span><span class="sxs-lookup"><span data-stu-id="a3c82-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="a3c82-224">ID3D12GraphicsCommandList:: Close</span><span class="sxs-lookup"><span data-stu-id="a3c82-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="a3c82-225">ID3D12GraphicsCommandList:: Копибуфферрегион</span><span class="sxs-lookup"><span data-stu-id="a3c82-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="a3c82-226">ID3D12GraphicsCommandList:: Копиресаурце</span><span class="sxs-lookup"><span data-stu-id="a3c82-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="a3c82-227">ID3D12GraphicsCommandList:: Копитекстуререгион</span><span class="sxs-lookup"><span data-stu-id="a3c82-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="a3c82-228">ID3D12GraphicsCommandList::D Patch</span><span class="sxs-lookup"><span data-stu-id="a3c82-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="a3c82-229">ID3D12GraphicsCommandList:: Ендевент</span><span class="sxs-lookup"><span data-stu-id="a3c82-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="a3c82-230">ID3D12GraphicsCommandList:: Ендкуери</span><span class="sxs-lookup"><span data-stu-id="a3c82-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="a3c82-231">ID3D12GraphicsCommandList:: Reset</span><span class="sxs-lookup"><span data-stu-id="a3c82-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="a3c82-232">ID3D12GraphicsCommandList:: Ресолвекуеридата</span><span class="sxs-lookup"><span data-stu-id="a3c82-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="a3c82-233">ID3D12GraphicsCommandList:: Ресаурцебарриер</span><span class="sxs-lookup"><span data-stu-id="a3c82-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="a3c82-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="a3c82-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="a3c82-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="a3c82-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="a3c82-236">ID3D12GraphicsCommandList:: Сеткомпутерутконстантбуффервиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="a3c82-237">ID3D12GraphicsCommandList:: Сеткомпутерутдескриптортабле</span><span class="sxs-lookup"><span data-stu-id="a3c82-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="a3c82-238">ID3D12GraphicsCommandList:: Сеткомпутерутшадерресаурцевиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="a3c82-239">ID3D12GraphicsCommandList:: Сеткомпутерутсигнатуре</span><span class="sxs-lookup"><span data-stu-id="a3c82-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="a3c82-240">ID3D12GraphicsCommandList:: Сеткомпутерутунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="a3c82-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="a3c82-241">ID3D12GraphicsCommandList:: Сетдескрипторхеапс</span><span class="sxs-lookup"><span data-stu-id="a3c82-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="a3c82-242">ID3D12GraphicsCommandList:: SetMarker</span><span class="sxs-lookup"><span data-stu-id="a3c82-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="a3c82-243">ID3D12GraphicsCommandList:: Сетпипелинестате</span><span class="sxs-lookup"><span data-stu-id="a3c82-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="a3c82-244">ID3D12GraphicsCommandList:: Сетпредикатион</span><span class="sxs-lookup"><span data-stu-id="a3c82-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="a3c82-245">Методы ID3D12GraphicsCommandList1</span><span class="sxs-lookup"><span data-stu-id="a3c82-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="a3c82-246">ID3D12GraphicsCommandList1:: Атомиккопибуфферуинт</span><span class="sxs-lookup"><span data-stu-id="a3c82-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="a3c82-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="a3c82-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="a3c82-248">Методы ID3D12GraphicsCommandList2</span><span class="sxs-lookup"><span data-stu-id="a3c82-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="a3c82-249">ID3D12GraphicsCommandList2:: Вритебуффериммедиате</span><span class="sxs-lookup"><span data-stu-id="a3c82-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="a3c82-250">Методы ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="a3c82-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="a3c82-251">ID3D12GraphicsCommandList4:: Ексекутеметакомманд</span><span class="sxs-lookup"><span data-stu-id="a3c82-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="a3c82-252">ID3D12GraphicsCommandList4:: Инитиализеметакомманд</span><span class="sxs-lookup"><span data-stu-id="a3c82-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)

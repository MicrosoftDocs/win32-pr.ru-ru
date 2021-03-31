---
description: 'В этом разделе содержатся сведения о следующих основных интерфейсах:'
ms.assetid: f5ad2db8-da90-4bcd-83a7-7466723a9c3c
title: Базовые интерфейсы Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c241def4bb0ab1064d924a7457c52e7197bc9199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423394"
---
# <a name="direct3d-10-core-interfaces"></a><span data-ttu-id="716e3-103">Базовые интерфейсы Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="716e3-103">Direct3D 10 core interfaces</span></span>

<span data-ttu-id="716e3-104">В этом разделе содержатся сведения о следующих основных интерфейсах:</span><span class="sxs-lookup"><span data-stu-id="716e3-104">This section contains information about the following core interfaces:</span></span>



| <span data-ttu-id="716e3-105">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="716e3-105">Interfaces</span></span>                                                           | <span data-ttu-id="716e3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="716e3-106">Description</span></span>                                         |
|----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="716e3-107">**Интерфейс ID3D10BlendState**</span><span class="sxs-lookup"><span data-stu-id="716e3-107">**ID3D10BlendState Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10blendstate)               | <span data-ttu-id="716e3-108">Обращается к состоянию смешения для устройства Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="716e3-108">Accesses blending state for a Direct3D 10.0 device.</span></span> |
| [<span data-ttu-id="716e3-109">**Интерфейс ID3D10BlendState1**</span><span class="sxs-lookup"><span data-stu-id="716e3-109">**ID3D10BlendState1 Interface**</span></span>](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)             | <span data-ttu-id="716e3-110">Обращается к состоянию смешения для устройства Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="716e3-110">Accesses blending state for a Direct3D 10.1 device.</span></span> |
| [<span data-ttu-id="716e3-111">**Интерфейс ID3D10DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="716e3-111">**ID3D10DepthStencilState Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilstate) | <span data-ttu-id="716e3-112">Доступ к состоянию шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="716e3-112">Accesses depth-stencil state.</span></span>                       |
| [<span data-ttu-id="716e3-113">**Интерфейс ID3D10InputLayout**</span><span class="sxs-lookup"><span data-stu-id="716e3-113">**ID3D10InputLayout Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout)             | <span data-ttu-id="716e3-114">Обращается к входным данным конвейера из памяти.</span><span class="sxs-lookup"><span data-stu-id="716e3-114">Accesses pipeline-input data from memory.</span></span>           |
| [<span data-ttu-id="716e3-115">**Интерфейс ID3D10RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="716e3-115">**ID3D10RasterizerState Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rasterizerstate)     | <span data-ttu-id="716e3-116">Доступ к состоянию средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="716e3-116">Accesses rasterizer state.</span></span>                          |
| [<span data-ttu-id="716e3-117">**Интерфейс ID3D10SamplerState**</span><span class="sxs-lookup"><span data-stu-id="716e3-117">**ID3D10SamplerState Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)           | <span data-ttu-id="716e3-118">Доступ к состоянию образца.</span><span class="sxs-lookup"><span data-stu-id="716e3-118">Accesses sampler state.</span></span>                             |



 



| <span data-ttu-id="716e3-119">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="716e3-119">Interfaces</span></span>                                                 | <span data-ttu-id="716e3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="716e3-120">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="716e3-121">**Интерфейс ID3D10Asynchronous**</span><span class="sxs-lookup"><span data-stu-id="716e3-121">**ID3D10Asynchronous Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10asynchronous) | <span data-ttu-id="716e3-122">Получает данные из GPU в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="716e3-122">Retrieves data from the GPU asynchronously.</span></span>                                          |
| [<span data-ttu-id="716e3-123">**Интерфейс ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="716e3-123">**ID3D10Blob Interface**</span></span>](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)                 | <span data-ttu-id="716e3-124">Возврат данных из памяти.</span><span class="sxs-lookup"><span data-stu-id="716e3-124">Return data from memory.</span></span>                                                             |
| [<span data-ttu-id="716e3-125">**Интерфейс ID3D10Counter**</span><span class="sxs-lookup"><span data-stu-id="716e3-125">**ID3D10Counter Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10counter)           | <span data-ttu-id="716e3-126">Измеряет производительность GPU.</span><span class="sxs-lookup"><span data-stu-id="716e3-126">Measures GPU performance.</span></span>                                                            |
| [<span data-ttu-id="716e3-127">**Интерфейс ID3D10Debug**</span><span class="sxs-lookup"><span data-stu-id="716e3-127">**ID3D10Debug Interface**</span></span>](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10debug)               | <span data-ttu-id="716e3-128">Включает или отключает слой отладки.</span><span class="sxs-lookup"><span data-stu-id="716e3-128">Enables/disables the debug layer.</span></span>                                                    |
| [<span data-ttu-id="716e3-129">**Интерфейс ID3D10Device**</span><span class="sxs-lookup"><span data-stu-id="716e3-129">**ID3D10Device Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)             | <span data-ttu-id="716e3-130">Представляет виртуальный адаптер для Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="716e3-130">Represents a virtual adapter for Direct3D 10.0.</span></span>                                      |
| [<span data-ttu-id="716e3-131">**Интерфейс ID3D10Device1**</span><span class="sxs-lookup"><span data-stu-id="716e3-131">**ID3D10Device1 Interface**</span></span>](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)           | <span data-ttu-id="716e3-132">Представляет виртуальный адаптер для Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="716e3-132">Represents a virtual adapter for Direct3D 10.1.</span></span>                                      |
| [<span data-ttu-id="716e3-133">**Интерфейс ID3D10DeviceChild**</span><span class="sxs-lookup"><span data-stu-id="716e3-133">**ID3D10DeviceChild Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10devicechild)   | <span data-ttu-id="716e3-134">Обращается к данным, используемым устройством.</span><span class="sxs-lookup"><span data-stu-id="716e3-134">Accesses data used by a device.</span></span>                                                      |
| <span data-ttu-id="716e3-135">[**Интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="716e3-135">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>           | <span data-ttu-id="716e3-136">Предоставляет определяемые пользователем методы для обработки включаемых файлов при загрузке результата.</span><span class="sxs-lookup"><span data-stu-id="716e3-136">Provides user-overridable methods for handling include files when loading an effect.</span></span> |
| [<span data-ttu-id="716e3-137">**Интерфейс ID3D10InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="716e3-137">**ID3D10InfoQueue Interface**</span></span>](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)       | <span data-ttu-id="716e3-138">Сохраняет, извлекает и фильтрует отладочные сообщения.</span><span class="sxs-lookup"><span data-stu-id="716e3-138">Stores, retrieves, and filters debug messages.</span></span>                                       |
| [<span data-ttu-id="716e3-139">**Интерфейс ID3D10Multithread**</span><span class="sxs-lookup"><span data-stu-id="716e3-139">**ID3D10Multithread Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10multithread)   | <span data-ttu-id="716e3-140">Обращается к многопотоковым параметрам.</span><span class="sxs-lookup"><span data-stu-id="716e3-140">Accesses multithread settings.</span></span>                                                       |
| [<span data-ttu-id="716e3-141">**Интерфейс ID3D10Predicate**</span><span class="sxs-lookup"><span data-stu-id="716e3-141">**ID3D10Predicate Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10predicate)       | <span data-ttu-id="716e3-142">Определяет, должна ли обрабатываться геометрия.</span><span class="sxs-lookup"><span data-stu-id="716e3-142">Determines whether geometry should be processed.</span></span>                                     |
| [<span data-ttu-id="716e3-143">**Интерфейс ID3D10Query**</span><span class="sxs-lookup"><span data-stu-id="716e3-143">**ID3D10Query Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10query)               | <span data-ttu-id="716e3-144">Запрашивает сведения из GPU.</span><span class="sxs-lookup"><span data-stu-id="716e3-144">Queries information from the GPU.</span></span>                                                    |
| [<span data-ttu-id="716e3-145">**Интерфейс ID3D10StateBlock**</span><span class="sxs-lookup"><span data-stu-id="716e3-145">**ID3D10StateBlock Interface**</span></span>](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock)     | <span data-ttu-id="716e3-146">Инкапсулирует состояния отрисовки.</span><span class="sxs-lookup"><span data-stu-id="716e3-146">Encapsulates render states.</span></span>                                                          |
| [<span data-ttu-id="716e3-147">**Интерфейс ID3D10SwitchToRef**</span><span class="sxs-lookup"><span data-stu-id="716e3-147">**ID3D10SwitchToRef Interface**</span></span>](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10switchtoref)   | <span data-ttu-id="716e3-148">Переключение между аппаратным и программным устройством.</span><span class="sxs-lookup"><span data-stu-id="716e3-148">Switches between a hardware and software device.</span></span>                                     |



 

<span data-ttu-id="716e3-149">Direct3D также импементс интерфейсы для:</span><span class="sxs-lookup"><span data-stu-id="716e3-149">Direct3D also impements interfaces for:</span></span>

-   [<span data-ttu-id="716e3-150">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="716e3-150">Resources</span></span>](d3d10-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="716e3-151">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="716e3-151">Shaders</span></span>](d3d10-graphics-reference-d3d10-shader-interfaces.md)
-   [<span data-ttu-id="716e3-152">Эффекты</span><span class="sxs-lookup"><span data-stu-id="716e3-152">Effects</span></span>](d3d10-graphics-reference-effect-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="716e3-153">См. также</span><span class="sxs-lookup"><span data-stu-id="716e3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716e3-154">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="716e3-154">Core Reference</span></span>](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 

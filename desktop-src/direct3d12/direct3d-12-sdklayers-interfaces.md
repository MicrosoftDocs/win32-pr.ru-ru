---
title: Интерфейсы слоя отладки
description: Следующие интерфейсы объявляются в d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "105650322"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="f13a6-103">Интерфейсы слоя отладки</span><span class="sxs-lookup"><span data-stu-id="f13a6-103">Debug Layer interfaces</span></span>

<span data-ttu-id="f13a6-104">Следующие интерфейсы определяются в `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="f13a6-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f13a6-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f13a6-105">In this section</span></span>

| <span data-ttu-id="f13a6-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="f13a6-106">Topic</span></span> | <span data-ttu-id="f13a6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f13a6-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="f13a6-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="f13a6-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="f13a6-109">Интерфейс отладки управляет параметрами отладки и проверяет состояние конвейера.</span><span class="sxs-lookup"><span data-stu-id="f13a6-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="f13a6-110">Его можно использовать только в том случае, если включен слой отладки.</span><span class="sxs-lookup"><span data-stu-id="f13a6-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="f13a6-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="f13a6-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="f13a6-112">Добавляется проверка на основе GPU и зависимая очередь команд на уровне отладки.</span><span class="sxs-lookup"><span data-stu-id="f13a6-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="f13a6-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="f13a6-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="f13a6-114">Добавляет настраиваемые уровни проверки GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="f13a6-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="f13a6-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="f13a6-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="f13a6-116">Добавляет в отладочный слой проверку на основе GPU, зависимую синхронизацию очереди команд и настраиваемые уровни проверки на основе GPU.</span><span class="sxs-lookup"><span data-stu-id="f13a6-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="f13a6-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="f13a6-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="f13a6-118">Предоставляет методы для мониторинга и отладки списка команд.</span><span class="sxs-lookup"><span data-stu-id="f13a6-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="f13a6-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="f13a6-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="f13a6-120">Этот интерфейс позволяет изменять параметры слоя отладки дополнительных списков команд.</span><span class="sxs-lookup"><span data-stu-id="f13a6-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="f13a6-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="f13a6-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="f13a6-122">Предоставляет методы для мониторинга и отладки очереди команд.</span><span class="sxs-lookup"><span data-stu-id="f13a6-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="f13a6-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="f13a6-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="f13a6-124">Этот интерфейс представляет графическое устройство для отладки.</span><span class="sxs-lookup"><span data-stu-id="f13a6-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="f13a6-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="f13a6-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="f13a6-126">Задает параметры уровня отладки для всего устройства.</span><span class="sxs-lookup"><span data-stu-id="f13a6-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="f13a6-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="f13a6-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="f13a6-128">Интерфейс очереди информации хранит, извлекает и фильтрует сообщения отладки.</span><span class="sxs-lookup"><span data-stu-id="f13a6-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="f13a6-129">Очередь состоит из очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения.</span><span class="sxs-lookup"><span data-stu-id="f13a6-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="f13a6-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="f13a6-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="f13a6-131">Часть контракта между диагностическими слоями D3D11On12 и инструментами диагностики графики.</span><span class="sxs-lookup"><span data-stu-id="f13a6-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f13a6-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f13a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13a6-133">Настройка среды программирования для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f13a6-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="f13a6-134">Справочник по слою отладки</span><span class="sxs-lookup"><span data-stu-id="f13a6-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="f13a6-135">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f13a6-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>
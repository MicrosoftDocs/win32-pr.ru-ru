---
title: Затенения
description: Затенения — это функция, которая позволяет GPU, а не ЦП определять, что не может рисовать, копировать или отправлять объект.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2020
ms.locfileid: "104549013"
---
# <a name="predication"></a><span data-ttu-id="ca71f-103">Затенения</span><span class="sxs-lookup"><span data-stu-id="ca71f-103">Predication</span></span>

<span data-ttu-id="ca71f-104">Затенения — это функция, которая позволяет GPU, а не ЦП определять, чтобы не рисовать, копировать или отправлять объект.</span><span class="sxs-lookup"><span data-stu-id="ca71f-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="ca71f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ca71f-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="ca71f-106">сетпредикатион</span><span class="sxs-lookup"><span data-stu-id="ca71f-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="ca71f-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ca71f-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="ca71f-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="ca71f-108">Overview</span></span>

<span data-ttu-id="ca71f-109">Обычно затенения используется с перекрытия; если ограничивающий прямоугольник нарисован и является перекрыто, то, очевидно, нет точки в рисовании самого объекта.</span><span class="sxs-lookup"><span data-stu-id="ca71f-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="ca71f-110">В этом случае рисование объекта может быть «predicateed», что позволяет его удалить из фактической отрисовки графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="ca71f-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="ca71f-111">На первый взгляд это может показаться редудантм и более поздним стандартным тестом глубины и более ранним этапом.</span><span class="sxs-lookup"><span data-stu-id="ca71f-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="ca71f-112">Но затенения может устранять издержки самого состояния команды рисования, а также растрирования.</span><span class="sxs-lookup"><span data-stu-id="ca71f-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="ca71f-113">Хотя ранний этап прохода удаляет ненужные пикселы, он по-прежнему может выполнять шейдеры вершин, поверхности, доменов и геометрии и вызывать входной ассемблер, тесселатор и средство программной прорисовки с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="ca71f-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="ca71f-114">Путем рисования простого ограничивающего прямоугольника или аналогичного ограничивающего тома, &mdash; который проще обрабатывать и растрирование, чем реальная модель &mdash; , можно избежать ненужного растрирования и обработки.</span><span class="sxs-lookup"><span data-stu-id="ca71f-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="ca71f-115">В отличие от Direct3D 11, затенения отделяется от запросов и расширяется в Direct3D 12, чтобы позволить приложению выполнять предикаты для объектов на основе любой причины, по которой разработчик приложения может принять решение (не только перекрытия).</span><span class="sxs-lookup"><span data-stu-id="ca71f-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="ca71f-116">сетпредикатион</span><span class="sxs-lookup"><span data-stu-id="ca71f-116">SetPredication</span></span>

<span data-ttu-id="ca71f-117">Затенения можно задать на основе значения 64-разрядов в буфере (см. [**D3D12 \_ затенения \_ Op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="ca71f-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="ca71f-118">Когда GPU выполняет команду [**сетпредикатион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , он привязывает значение в буфере.</span><span class="sxs-lookup"><span data-stu-id="ca71f-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="ca71f-119">Будущие изменения данных в буфере не задним числом влияют на состояние затенения.</span><span class="sxs-lookup"><span data-stu-id="ca71f-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="ca71f-120">Если входной буфер параметров имеет значение NULL, затенения отключен.</span><span class="sxs-lookup"><span data-stu-id="ca71f-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="ca71f-121">Указания затенения отсутствуют в API Direct3D 12. и затенения разрешены в списках команд Direct, COMPUTE и Copy.</span><span class="sxs-lookup"><span data-stu-id="ca71f-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="ca71f-122">Исходный буфер может находиться в любом типе кучи (по умолчанию, upload, реадбакк, Custom).</span><span class="sxs-lookup"><span data-stu-id="ca71f-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="ca71f-123">Основная среда выполнения будет проверять следующее:</span><span class="sxs-lookup"><span data-stu-id="ca71f-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="ca71f-124">*Алигнедбуффероффсет* имеет размер, кратный 8 байтам</span><span class="sxs-lookup"><span data-stu-id="ca71f-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="ca71f-125">Ресурс является буфером.</span><span class="sxs-lookup"><span data-stu-id="ca71f-125">The resource is a buffer</span></span>
-   <span data-ttu-id="ca71f-126">Операция является допустимым членом перечисления</span><span class="sxs-lookup"><span data-stu-id="ca71f-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="ca71f-127">[**Сетпредикатион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) не может быть вызван из пакета</span><span class="sxs-lookup"><span data-stu-id="ca71f-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="ca71f-128">Тип списка команд поддерживает затенения</span><span class="sxs-lookup"><span data-stu-id="ca71f-128">The command list type supports predication</span></span>
-   <span data-ttu-id="ca71f-129">Смещение не превышает размер буфера</span><span class="sxs-lookup"><span data-stu-id="ca71f-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="ca71f-130">Отладочный слой выдаст ошибку, если исходный буфер не находится в [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (который совпадает с [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)и просто псевдонимом).</span><span class="sxs-lookup"><span data-stu-id="ca71f-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="ca71f-131">Набор операций, которые могут быть предикатами:</span><span class="sxs-lookup"><span data-stu-id="ca71f-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="ca71f-132">**дравинстанцед**</span><span class="sxs-lookup"><span data-stu-id="ca71f-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="ca71f-133">**дравиндексединстанцед**</span><span class="sxs-lookup"><span data-stu-id="ca71f-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="ca71f-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="ca71f-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="ca71f-135">**копитекстуререгион**</span><span class="sxs-lookup"><span data-stu-id="ca71f-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="ca71f-136">**копибуфферрегион**</span><span class="sxs-lookup"><span data-stu-id="ca71f-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="ca71f-137">**копиресаурце**</span><span class="sxs-lookup"><span data-stu-id="ca71f-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="ca71f-138">**копитилес**</span><span class="sxs-lookup"><span data-stu-id="ca71f-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="ca71f-139">**ресолвесубресаурце**</span><span class="sxs-lookup"><span data-stu-id="ca71f-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="ca71f-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="ca71f-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="ca71f-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="ca71f-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="ca71f-142">**клеарунордередакцессвиевуинт**</span><span class="sxs-lookup"><span data-stu-id="ca71f-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="ca71f-143">**клеарунордередакцессвиевфлоат**</span><span class="sxs-lookup"><span data-stu-id="ca71f-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="ca71f-144">**ексекутеиндирект**</span><span class="sxs-lookup"><span data-stu-id="ca71f-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="ca71f-145">[**Ексекутебундле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) не является самим предикатом.</span><span class="sxs-lookup"><span data-stu-id="ca71f-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="ca71f-146">Вместо этого отдельные операции из приведенного выше списка, содержащиеся в конце пакета, объединяются в предикате.</span><span class="sxs-lookup"><span data-stu-id="ca71f-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="ca71f-147">Методы ID3D12GraphicsCommandList [**ресолвекуеридата**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**бегинкуери**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) и [**ендкуери**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) не являются предикатами.</span><span class="sxs-lookup"><span data-stu-id="ca71f-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca71f-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ca71f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca71f-149">Счетчики и запросы</span><span class="sxs-lookup"><span data-stu-id="ca71f-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="ca71f-150">Измерение производительности</span><span class="sxs-lookup"><span data-stu-id="ca71f-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="ca71f-151">Пошаговые инструкции по запросам затенения</span><span class="sxs-lookup"><span data-stu-id="ca71f-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 





---
title: Различия в модели привязки от Direct3D 11
description: Одним из основных решений по проектированию привязок DirectX12 является отделение ее от других задач управления. Это помещает некоторые требования к приложению для управления определенными потенциальными причинами опасности.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104850"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a><span data-ttu-id="d5e3b-104">Различия в модели привязки от Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d5e3b-104">Differences in the Binding Model from Direct3D 11</span></span>

<span data-ttu-id="d5e3b-105">Одним из основных решений по проектированию привязок DirectX12 является отделение ее от других задач управления.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-105">One of the main design decisions behind DirectX12 binding is to separate it from other management tasks.</span></span> <span data-ttu-id="d5e3b-106">Это помещает некоторые требования к приложению для управления определенными потенциальными причинами опасности.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-106">This places some requirements on the app to manage certain potential hazards.</span></span>

<span data-ttu-id="d5e3b-107">Основное преимущество модели привязки D3D12 заключается в том, что она позволяет приложениям часто изменять привязки текстур без затрат на производительность ЦП.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-107">The main advantage of the D3D12 Binding Model is that it enables apps to change texture bindings frequently, without a huge CPU performance cost.</span></span> <span data-ttu-id="d5e3b-108">Другими преимуществами является то, что шейдеры имеют доступ к очень большому количеству ресурсов, шейдеру не нужно заранее знать, сколько ресурсов будет привязано, и что можно использовать унифицированную модель привязки ресурсов независимо от оборудования или потока содержимого приложений.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-108">Other benefits are that shaders have access to a very large number of resources, shaders need not know in advance how many resources will be bound, and that a unified resource binding model can be used regardless of hardware or the apps content flow.</span></span>

<span data-ttu-id="d5e3b-109">Для повышения производительности в модели привязки не требуется, чтобы система следит за тем, какие привязки приложение запросило использовать GPU, и существует чистая интеграция между привязками и списками команд с несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-109">To improve performance, the binding model does not require the system to keep track of what bindings an app has requested the GPU to use, and there is a clean integration between binding and multi-threaded command lists.</span></span>

<span data-ttu-id="d5e3b-110">В следующих разделах перечислены некоторые изменения в модели привязки ресурсов с момента D3D11.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-110">The following sections list some of the changes to the resource binding model since D3D11.</span></span>

-   [<span data-ttu-id="d5e3b-111">Управление местонахождение памяти, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-111">Memory Residency Management Separated From Binding</span></span>](#memory-residency-management-separated-from-binding)
-   [<span data-ttu-id="d5e3b-112">Управление жизненным циклом объектов, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-112">Object Lifetime Management Separated From Binding</span></span>](#object-lifetime-management-separated-from-binding)
-   [<span data-ttu-id="d5e3b-113">Отслеживание состояния ресурсов драйвера, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-113">Driver Resource State Tracking Separated From Binding</span></span>](#driver-resource-state-tracking-separated-from-binding)
-   [<span data-ttu-id="d5e3b-114">Синхронизация сопоставленной памяти GPU ЦП, отделенной от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-114">CPU GPU Mapped Memory Synchronization Separated From Binding</span></span>](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [<span data-ttu-id="d5e3b-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d5e3b-115">Related topics</span></span>](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a><span data-ttu-id="d5e3b-116">Управление местонахождение памяти, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-116">Memory Residency Management Separated From Binding</span></span>

<span data-ttu-id="d5e3b-117">Приложения имеют явный контроль над тем, какие поверхности они должны быть доступны для непосредственного использования GPU (называемого «резидентным»).</span><span class="sxs-lookup"><span data-stu-id="d5e3b-117">Applications have explicit control over which surfaces they need to be available for the GPU to use directly (called being "resident").</span></span> <span data-ttu-id="d5e3b-118">И наоборот, они могут применить другие состояния к ресурсам, например явно сделать их нерезидентными или позволить операционной системе выбирать определенные классы приложений, требующих минимального объема памяти.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-118">Conversely, they can apply other states on resources such as explicitly making them not resident, or letting the OS choose for certain classes of applications that require a minimal memory footprint.</span></span> <span data-ttu-id="d5e3b-119">Важно отметить, что Управление приложением того, что является резидентным, полностью отделяется от того, как оно предоставляет доступ к ресурсам для шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-119">The important point here is that the application's management of what is resident is completely decoupled from how it gives access to resources to shaders.</span></span>

<span data-ttu-id="d5e3b-120">Отделение управления местонахождение от механизма предоставления шейдерам доступа к ресурсам снижает затраты на систему и оборудование для отрисовки, поскольку ОС не обязательно постоянно проверять состояние локальной привязки, чтобы узнать, что делать в резидентном режиме.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-120">The decoupling of residency management from the mechanism for giving shaders access to resources reduces the system/hardware cost for rendering since the OS doesn't have to constantly inspect the local binding state to know what to make resident.</span></span> <span data-ttu-id="d5e3b-121">Более того, шейдеру больше не нужно знать, какие точные поверхности могут ссылаться на них, если весь набор потенциально доступных ресурсов был заранее создан в резиденте.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-121">Furthermore, shaders no longer have to know which exact surfaces they may need to reference, as long as the entire set of possibly accessible resources has been made resident ahead of time.</span></span>

## <a name="object-lifetime-management-separated-from-binding"></a><span data-ttu-id="d5e3b-122">Управление жизненным циклом объектов, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-122">Object Lifetime Management Separated From Binding</span></span>

<span data-ttu-id="d5e3b-123">В отличие от предыдущих API, система больше не отслеживает привязки ресурсов в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-123">Unlike previous APIs, the system no longer tracks bindings of resources to the pipeline.</span></span> <span data-ttu-id="d5e3b-124">Это позволяет системе поддерживать ресурсы активности, выпущенные приложением, так как на них по-прежнему ссылаются невыполненные работы GPU.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-124">This used to enable the system to keep alive resources that the application has released because they are still referenced by outstanding GPU work.</span></span>

<span data-ttu-id="d5e3b-125">Прежде чем освободить любой ресурс, например текстуру, необходимо убедиться, что GPU завершил создание ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-125">Before freeing any resource, such as a texture, applications now must make sure the GPU has completed referencing it.</span></span> <span data-ttu-id="d5e3b-126">Это означает, что прежде чем приложение сможет безопасно освободить ресурс, графический процессор должен завершить выполнение списка команд, ссылающегося на ресурс.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-126">This means before an application can safely free a resource the GPU must have completed execution of the command list referencing the resource.</span></span>

## <a name="driver-resource-state-tracking-separated-from-binding"></a><span data-ttu-id="d5e3b-127">Отслеживание состояния ресурсов драйвера, отделенное от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-127">Driver Resource State Tracking Separated From Binding</span></span>

<span data-ttu-id="d5e3b-128">Система больше не проверяет привязки ресурсов, чтобы понять, когда произошел переход ресурсов, требующий дополнительного использования драйвера или GPU.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-128">The system no longer inspects resource bindings to understand when resource transitions have occurred which require additional driver or GPU work.</span></span> <span data-ttu-id="d5e3b-129">Распространенным примером многих GPU и драйверов является необходимость узнать, когда поверхность используется в качестве целевого представления отрисовки (РТВ) для шейдера представление ресурсов (SRV).</span><span class="sxs-lookup"><span data-stu-id="d5e3b-129">A common example for many GPUs and drivers is having to know when a surface transitions from being used as a Render Target View (RTV) to Shader Resource View (SRV).</span></span> <span data-ttu-id="d5e3b-130">Сами приложения теперь должны выделять, когда какие-либо переходы по ресурсам, которые может отслеживать система, происходят через выделенные API.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-130">Applications themselves must now identify when any resource transitions that the system might care about are happening via dedicated APIs.</span></span>

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a><span data-ttu-id="d5e3b-131">Синхронизация сопоставленной памяти GPU ЦП, отделенной от привязки</span><span class="sxs-lookup"><span data-stu-id="d5e3b-131">CPU GPU Mapped Memory Synchronization Separated From Binding</span></span>

<span data-ttu-id="d5e3b-132">Система больше не проверяет привязки ресурсов, чтобы понять, нужно ли отложить обработку, поскольку она зависит от ресурса, который был сопоставлен для доступа к ЦП, но еще не сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-132">The system no longer inspects resource bindings to understand if rendering needs to be delayed because it depends on a resource that has been mapped for CPU access but has not been unmapped yet.</span></span> <span data-ttu-id="d5e3b-133">Теперь у приложений есть ответственность за синхронизацию доступа к памяти ЦП и GPU.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-133">Applications now have the responsibility to synchronize CPU and GPU memory accesses.</span></span> <span data-ttu-id="d5e3b-134">Для этого система предоставляет механизмы, позволяющие приложению запрашивать спящий режим потока ЦП до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-134">To help with this, the system provides mechanisms for the application to request the sleeping of a CPU thread until work completes.</span></span> <span data-ttu-id="d5e3b-135">Опрос также может быть выполнен, но может быть менее эффективным.</span><span class="sxs-lookup"><span data-stu-id="d5e3b-135">Polling could also be done, but can be less efficient.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5e3b-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d5e3b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5e3b-137">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5e3b-137">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





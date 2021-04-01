---
description: Интерфейс IDirect3DDevice9 поддерживает обработку вершин в программном и аппаратном обеспечении.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Обработка данных вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894942"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="97377-103">Обработка данных вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="97377-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="97377-104">Интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) поддерживает обработку вершин в программном и аппаратном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="97377-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="97377-105">Как правило, возможности устройства для обработки вершин программного и аппаратного обеспечения не идентичны.</span><span class="sxs-lookup"><span data-stu-id="97377-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="97377-106">Аппаратные возможности являются переменными, в зависимости от видеоадаптера и драйвера, в то время как возможности программного обеспечения устранены.</span><span class="sxs-lookup"><span data-stu-id="97377-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="97377-107">Следующие флаги управляют поведением обработки вершин для слоя абстрагирования оборудования (HAL) и ссылочных устройств.</span><span class="sxs-lookup"><span data-stu-id="97377-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="97377-108">D3DCREATE \_ Software \_ вертекспроцессинг</span><span class="sxs-lookup"><span data-stu-id="97377-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="97377-109">D3DCREATE \_ оборудование \_ вертекспроцессинг</span><span class="sxs-lookup"><span data-stu-id="97377-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="97377-110">D3DCREATE \_ Mixed \_ вертекспроцессинг</span><span class="sxs-lookup"><span data-stu-id="97377-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="97377-111">Укажите один из флагов поведения обработки вершин при вызове [**IDirect3D9:: креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="97377-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="97377-112">Флаг смешанного режима позволяет устройству выполнять обработку вершин программного и аппаратного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="97377-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="97377-113">Только один флаг обработки вершин может быть установлен для устройства в один момент времени.</span><span class="sxs-lookup"><span data-stu-id="97377-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="97377-114">Обратите внимание, \_ что \_ при создании чистого устройства (D3DCREATE пуредевице) должен быть установлен флаг D3DCREATE Hardware вертекспроцессинг \_ .</span><span class="sxs-lookup"><span data-stu-id="97377-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="97377-115">Чтобы избежать возможности обработки двух вершин на одном устройстве, во время выполнения могут быть запрошены только возможности аппаратной обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="97377-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="97377-116">Возможности обработки вершин программного обеспечения являются фиксированными и не могут быть запрошены во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="97377-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="97377-117">Элемент Вертекспроцессингкапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) определяет возможности устройства по аппаратной обработке вершин.</span><span class="sxs-lookup"><span data-stu-id="97377-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="97377-118">Для обработки вершин программного обеспечения поддерживаются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="97377-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="97377-119">член D3DVTXPCAPS \_ Директионаллигхтс [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="97377-120">член D3DVTXPCAPS \_ Локалвиевер [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="97377-121">член D3DVTXPCAPS \_ MATERIALSOURCE7 [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="97377-122">член D3DVTXPCAPS \_ Поситионаллигхтс [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="97377-123">член D3DVTXPCAPS \_ Тексжен [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="97377-124">\_элемент анимации D3DVTXPCAPS элемента [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="97377-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="97377-125">Кроме того, в следующей таблице перечислены значения, заданные для элементов структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства в режиме обработки вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="97377-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="97377-126">Член</span><span class="sxs-lookup"><span data-stu-id="97377-126">Member</span></span>                 | <span data-ttu-id="97377-127">Возможности обработки вершин программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="97377-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="97377-128">максактивелигхтс</span><span class="sxs-lookup"><span data-stu-id="97377-128">MaxActiveLights</span></span>        | <span data-ttu-id="97377-129">Неограниченно</span><span class="sxs-lookup"><span data-stu-id="97377-129">Unlimited</span></span>                               |
| <span data-ttu-id="97377-130">максусерклиппланес</span><span class="sxs-lookup"><span data-stu-id="97377-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="97377-131">6</span><span class="sxs-lookup"><span data-stu-id="97377-131">6</span></span>                                       |
| <span data-ttu-id="97377-132">максвертексблендматрицес</span><span class="sxs-lookup"><span data-stu-id="97377-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="97377-133">4</span><span class="sxs-lookup"><span data-stu-id="97377-133">4</span></span>                                       |
| <span data-ttu-id="97377-134">максстреамс</span><span class="sxs-lookup"><span data-stu-id="97377-134">MaxStreams</span></span>             | <span data-ttu-id="97377-135">16</span><span class="sxs-lookup"><span data-stu-id="97377-135">16</span></span>                                      |
| <span data-ttu-id="97377-136">максвертексиндекс</span><span class="sxs-lookup"><span data-stu-id="97377-136">MaxVertexIndex</span></span>         | <span data-ttu-id="97377-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="97377-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="97377-138">Как правило, любое приложение, для которого привязана обработка вершин, должно использовать устройство HAL.</span><span class="sxs-lookup"><span data-stu-id="97377-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="97377-139">Обработка вершин программного обеспечения обеспечивает гарантированный набор возможностей обработки вершин, включая неограниченное число источников света и полную поддержку программируемых шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="97377-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="97377-140">Можно переключаться между обработкой вершин программного обеспечения и оборудования в любое время при использовании устройства HAL (это единственный тип устройства, поддерживающий как аппаратную, так и программную обработку вершин).</span><span class="sxs-lookup"><span data-stu-id="97377-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="97377-141">Единственное требование заключается в том, что буферы вершин, используемые для обработки вершин программного обеспечения, должны выделяться в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="97377-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97377-142">См. также</span><span class="sxs-lookup"><span data-stu-id="97377-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97377-143">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="97377-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 

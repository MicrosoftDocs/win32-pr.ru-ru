---
title: Основные интерфейсы Direct3D 11
description: В этом разделе содержатся сведения об основных интерфейсах.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- интерфейсы, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488425"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="d9bdd-104">Основные интерфейсы Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d9bdd-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="d9bdd-105">В этом разделе содержатся сведения об основных интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9bdd-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d9bdd-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9bdd-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="d9bdd-107">Topic</span></span></th>
<th><span data-ttu-id="d9bdd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d9bdd-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9bdd-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-110">Этот интерфейс инкапсулирует методы для асинхронного извлечения данных из GPU.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-112">Интерфейс состояния Blend содержит описание состояния наложения, которое можно привязать к <a href="d3d10-graphics-programming-guide-output-merger-stage.md">этапу слияния вывода</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-114">Интерфейс состояния Blend содержит описание состояния наложения, которое можно привязать к <a href="d3d10-graphics-programming-guide-output-merger-stage.md">этапу слияния вывода</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="d9bdd-115">Этот интерфейс состояния Blend поддерживает логические операции, а также операции смешения.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-117">Интерфейс <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> инкапсулирует список графических команд для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-119">Этот интерфейс инкапсулирует методы для измерения производительности GPU.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-121">Интерфейс состояния "Глубина-трафарет" содержит описание состояния шаблона глубины, которое можно привязать к <a href="d3d10-graphics-programming-guide-output-merger-stage.md">этапу слияния вывода</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-123">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-125">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="d9bdd-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-128">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="d9bdd-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-131">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="d9bdd-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-134">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="d9bdd-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> добавляет новые методы в <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, такие как <strong>регистердевицеремоведевент</strong> и <strong>унрегистердевицеремовед</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-137">Интерфейс устройства представляет виртуальный адаптер; Он используется для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="d9bdd-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-140">Дочерний интерфейс устройства получает доступ к данным, используемым устройством.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-142">Интерфейс <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a> представляет контекст устройства, который создает команды отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d9bdd-143">Последняя версия этого интерфейса — <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> , представленная в обновлении Windows 10 для дизайнеров.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="d9bdd-144">Приложения предназначенных Windows 10 Creators Update должны использовать интерфейс <strong>ID3D11DeviceContext4</strong> вместо <strong>ID3D11Device</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-146">Интерфейс контекста устройства представляет контекст устройства; Он используется для визуализации команд.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="d9bdd-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-149">Интерфейс контекста устройства представляет контекст устройства; Он используется для визуализации команд.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="d9bdd-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-152">Интерфейс контекста устройства представляет контекст устройства; Он используется для визуализации команд.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="d9bdd-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-155">Интерфейс контекста устройства представляет контекст устройства; Он используется для визуализации команд.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="d9bdd-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> добавляет новые методы к элементам в <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-158">Интерфейс <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> представляет объект состояния контекста, который содержит сведения о состоянии и поведении для устройства Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-160">Представляет ограждение, объект, используемый для синхронизации ЦП и один или несколько GPU.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-162">Интерфейс макета ввода содержит определение того, как передавать данные вершин, размещенные в памяти, в <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">этап ассемблерного</a> <a href="overviews-direct3d-11-graphics-pipeline.md">конвейера</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-164">Обеспечивает защиту потоков для критически важных частей многопоточного приложения.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-166">Интерфейс предиката определяет, должна ли быть обработана геометрия в зависимости от результатов предыдущего вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-168">Интерфейс запроса запрашивает информацию из GPU.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-170">Представляет объект запроса для запроса сведений из графического процессора.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-172">Интерфейс состояния средства программной прорисовки содержит описание состояния средства растеризации, которое можно привязать к <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">этапу средства прорисовки</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-174">Интерфейс состояния средства программной прорисовки содержит описание состояния средства растеризации, которое можно привязать к <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">этапу средства прорисовки</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="d9bdd-175">Этот интерфейс состояния средства отображения программной прорисовки поддерживает принудительное число выборок.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9bdd-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-177">Интерфейс состояния средства программной прорисовки содержит описание состояния средства растеризации, которое можно привязать к <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">этапу средства прорисовки</a>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="d9bdd-178">Этот интерфейс состояния средства отображения программной прорисовки поддерживает принудительное число выборок и консервативный режим растрирования.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9bdd-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9bdd-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="d9bdd-180">В интерфейсе состояния выборки содержится описание состояния образца, которое можно привязать к любому этапу шейдера <a href="overviews-direct3d-11-graphics-pipeline.md">конвейера</a> для ссылки на операции выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d9bdd-181">Direct3D 11 реализует интерфейсы для:</span><span class="sxs-lookup"><span data-stu-id="d9bdd-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="d9bdd-182">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9bdd-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="d9bdd-183">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="d9bdd-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="d9bdd-184">См. также</span><span class="sxs-lookup"><span data-stu-id="d9bdd-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bdd-185">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="d9bdd-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>


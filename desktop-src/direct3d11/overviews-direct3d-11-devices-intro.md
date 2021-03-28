---
title: Общие сведения об устройстве в Direct3D 11
description: Объектная модель Direct3D 11 разделяет функции создания и отрисовки ресурсов в устройство и один или несколько контекстов. Это разделение предназначено для упрощения многопоточности.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983685"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="7e288-103">Общие сведения об устройстве в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7e288-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="7e288-104">Объектная модель Direct3D 11 разделяет функции создания и отрисовки ресурсов в устройство и один или несколько контекстов. Это разделение предназначено для упрощения многопоточности.</span><span class="sxs-lookup"><span data-stu-id="7e288-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="7e288-105">Устройство</span><span class="sxs-lookup"><span data-stu-id="7e288-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="7e288-106">Контекст устройства</span><span class="sxs-lookup"><span data-stu-id="7e288-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="7e288-107">Контекст интерпретации</span><span class="sxs-lookup"><span data-stu-id="7e288-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="7e288-108">Отложенный контекст</span><span class="sxs-lookup"><span data-stu-id="7e288-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="7e288-109">Особенности работы с потоками</span><span class="sxs-lookup"><span data-stu-id="7e288-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="7e288-110">См. также</span><span class="sxs-lookup"><span data-stu-id="7e288-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="7e288-111">Устройство</span><span class="sxs-lookup"><span data-stu-id="7e288-111">Device</span></span>

<span data-ttu-id="7e288-112">Устройство используется для создания ресурсов и перечисления возможностей видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="7e288-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="7e288-113">В Direct3D 11 устройство представлено с интерфейсом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="7e288-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="7e288-114">К каждого приложения должно быть хотя бы одно устройство; большинство приложений создают только одно устройство.</span><span class="sxs-lookup"><span data-stu-id="7e288-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="7e288-115">Создайте устройство для одного из драйверов оборудования, установленных на компьютере, вызвав [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) или [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) и указав тип драйвера с флагом [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="7e288-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="7e288-116">Каждое устройство можно использовать один или несколько контекстов устройств, в зависимости от требуемой функциональности.</span><span class="sxs-lookup"><span data-stu-id="7e288-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="7e288-117">Контекст устройства</span><span class="sxs-lookup"><span data-stu-id="7e288-117">Device Context</span></span>

<span data-ttu-id="7e288-118">Контекст устройства содержит условия или настройки, в которых используется устройство.</span><span class="sxs-lookup"><span data-stu-id="7e288-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="7e288-119">В частности, контекст устройства используется для задания состояния конвейера и создания команд отрисовки с использованием ресурсов, принадлежащих устройству.</span><span class="sxs-lookup"><span data-stu-id="7e288-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="7e288-120">В Direct3D 11 реализованы два типа контекстов устройств: один для немедленной визуализации, другой — для отложенной отрисовки. Оба контекста представлены интерфейсом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="7e288-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="7e288-121">Контекст интерпретации</span><span class="sxs-lookup"><span data-stu-id="7e288-121">Immediate Context</span></span>

<span data-ttu-id="7e288-122">Непосредственный контекст переводится непосредственно в драйвер.</span><span class="sxs-lookup"><span data-stu-id="7e288-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="7e288-123">Каждое устройство имеет только один непосредственный контекст, который может получать данные из GPU.</span><span class="sxs-lookup"><span data-stu-id="7e288-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="7e288-124">Непосредственный контекст можно использовать для немедленного отображения (или воспроизведения) [списка команд](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="7e288-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="7e288-125">Существует два способа получить непосредственный контекст:</span><span class="sxs-lookup"><span data-stu-id="7e288-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="7e288-126">Путем вызова либо [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) , либо [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="7e288-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="7e288-127">Путем вызова [**ID3D11Device:: жетиммедиатеконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="7e288-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="7e288-128">Отложенный контекст</span><span class="sxs-lookup"><span data-stu-id="7e288-128">Deferred Context</span></span>

<span data-ttu-id="7e288-129">Отложенный контекст записывает команды GPU в [список команд](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="7e288-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="7e288-130">Отложенный контекст в основном используется для многопоточности и не является обязательным для однопотокового приложения.</span><span class="sxs-lookup"><span data-stu-id="7e288-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="7e288-131">Отложенный контекст обычно используется рабочим потоком вместо основного потока отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7e288-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="7e288-132">При создании отложенного контекста он не наследует никаких состояний от непосредственных контекстов.</span><span class="sxs-lookup"><span data-stu-id="7e288-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="7e288-133">Чтобы получить отложенный контекст, вызовите метод [**ID3D11Device:: креатедеферредконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="7e288-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="7e288-134">Любой контекст — немедленное или отложенное — может использоваться в любом потоке, если контекст используется только в одном потоке за раз.</span><span class="sxs-lookup"><span data-stu-id="7e288-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="7e288-135">Особенности работы с потоками</span><span class="sxs-lookup"><span data-stu-id="7e288-135">Threading Considerations</span></span>

<span data-ttu-id="7e288-136">В этой таблице показаны различия в модели потоков в Direct3D 11 от предыдущих версий Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7e288-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e288-137">Различия между Direct3D 11 и предыдущими версиями Direct3D:</span><span class="sxs-lookup"><span data-stu-id="7e288-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="7e288-138">Все методы интерфейса <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> являются свободными потоками, что означает, что несколько потоков могут вызывать функции одновременно.</span><span class="sxs-lookup"><span data-stu-id="7e288-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="7e288-139">Все интерфейсы, производные от <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>и т. д.), являются свободными потоками.</span><span class="sxs-lookup"><span data-stu-id="7e288-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="7e288-140">Direct3D 11 разделяет ресурсы на создание и визуализацию в двух интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="7e288-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="7e288-141">Сопоставление, отмена сопоставления, начало, конец и метод GetData реализуются в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a> , так как <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> строго определяет порядок операций.</span><span class="sxs-lookup"><span data-stu-id="7e288-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="7e288-142">Интерфейсы <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> и <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> также реализуют методы для операций, выполняемых в произвольных потоках.</span><span class="sxs-lookup"><span data-stu-id="7e288-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="7e288-143">Методы <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ссылку ID3D11DeviceContext</strong></a> (за исключением тех, которые существуют в <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) не являются потокобезопасными, то есть для них требуется единая Организация.</span><span class="sxs-lookup"><span data-stu-id="7e288-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="7e288-144">Только один поток может безопасно вызывать любой из его методов (рисования, копирования, сопоставлений и т. д.) за раз.</span><span class="sxs-lookup"><span data-stu-id="7e288-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="7e288-145">Как правило, при свободной многопоточности уменьшается количество используемых примитивов синхронизации, а также их длительность.</span><span class="sxs-lookup"><span data-stu-id="7e288-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="7e288-146">Однако приложение, которое использует синхронизацию в течение длительного времени, может напрямую влиять на то, сколько параллелизма может быть достигнуто приложением.</span><span class="sxs-lookup"><span data-stu-id="7e288-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="7e288-147">Методы интерфейса ID3D10Device не предназначены для бессвинцовых потоков.</span><span class="sxs-lookup"><span data-stu-id="7e288-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="7e288-148">ID3D10Device реализует все функции создания и отрисовки (как и ID3D9Device в Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="7e288-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="7e288-149">Map и unend реализуются в интерфейсах, производных от ID3D10Resource, Begin, End и GetData реализуются в интерфейсах, производных от ID3D10Asynchronous.</span><span class="sxs-lookup"><span data-stu-id="7e288-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7e288-150">См. также</span><span class="sxs-lookup"><span data-stu-id="7e288-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e288-151">Устройства</span><span class="sxs-lookup"><span data-stu-id="7e288-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 






---
title: Программные уровни
description: Среда выполнения Direct3D 11 создается с использованием слоев, начиная с базовой функциональности ядра и создавая необязательные функции и возможности для разработчиков во внешних слоях. В этом разделе описываются функциональные возможности каждого слоя.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533191"
---
# <a name="software-layers"></a><span data-ttu-id="ee330-104">Программные уровни</span><span class="sxs-lookup"><span data-stu-id="ee330-104">Software Layers</span></span>

<span data-ttu-id="ee330-105">Среда выполнения Direct3D 11 создается с использованием слоев, начиная с базовой функциональности ядра и создавая необязательные функции и возможности для разработчиков во внешних слоях.</span><span class="sxs-lookup"><span data-stu-id="ee330-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="ee330-106">В этом разделе описываются функциональные возможности каждого слоя.</span><span class="sxs-lookup"><span data-stu-id="ee330-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="ee330-107">Как правило, слои добавляют функциональные возможности, но не изменяют существующее поведение.</span><span class="sxs-lookup"><span data-stu-id="ee330-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="ee330-108">Например, основные функции будут иметь одинаковые возвращаемые значения независимо от создаваемого слоя отладки, хотя при создании экземпляра слоя отладки могут быть предоставлены дополнительные выходные данные отладки.</span><span class="sxs-lookup"><span data-stu-id="ee330-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="ee330-109">Чтобы создать слои при создании устройства, вызовите [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) или [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) и укажите один или несколько [**D3D11 создать значения \_ \_ \_ флага устройства**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .</span><span class="sxs-lookup"><span data-stu-id="ee330-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="ee330-110">Direct3D 11 предоставляет следующие уровни среды выполнения:</span><span class="sxs-lookup"><span data-stu-id="ee330-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="ee330-111">Уровень ядра</span><span class="sxs-lookup"><span data-stu-id="ee330-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="ee330-112">Отладочный слой</span><span class="sxs-lookup"><span data-stu-id="ee330-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="ee330-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ee330-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="ee330-114">Уровень ядра</span><span class="sxs-lookup"><span data-stu-id="ee330-114">Core Layer</span></span>

<span data-ttu-id="ee330-115">Основной слой существует по умолчанию. обеспечение очень тонкого сопоставления между API и драйвером устройства, что сводит к минимуму затраты на вызовы с высокой частотой.</span><span class="sxs-lookup"><span data-stu-id="ee330-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="ee330-116">Поскольку основной уровень является важным для производительности, он выполняет только критическую проверку.</span><span class="sxs-lookup"><span data-stu-id="ee330-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="ee330-117">Остальные слои являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="ee330-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="ee330-118">Отладочный слой</span><span class="sxs-lookup"><span data-stu-id="ee330-118">Debug Layer</span></span>

<span data-ttu-id="ee330-119">Слой отладки предоставляет широкие возможности проверки целостности и согласованности (например, проверка компоновки шейдера и привязки ресурсов, проверка согласованности параметров и сообщения об ошибках).</span><span class="sxs-lookup"><span data-stu-id="ee330-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="ee330-120">Чтобы создать устройство, поддерживающее уровень отладки, необходимо установить пакет SDK DirectX (для получения D3D11SDKLayers.dll), а затем указать флаг **D3D11 \_ Create \_ Device \_ Debug** при вызове функции [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) или функции [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) .</span><span class="sxs-lookup"><span data-stu-id="ee330-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="ee330-121">Если приложение запускается с включенным уровнем отладки, приложение будет работать значительно медленнее.</span><span class="sxs-lookup"><span data-stu-id="ee330-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="ee330-122">Но чтобы гарантировать, что приложение будет очищать ошибки и предупреждения перед отправкой, используйте отладочный слой.</span><span class="sxs-lookup"><span data-stu-id="ee330-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="ee330-123">Дополнительные сведения см. в разделе [Использование отладочного слоя для отладки приложений](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="ee330-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="ee330-124">Для создания устройства, поддерживающего уровень отладки Windows 7 с обновлением платформы для Windows 7 (KB2670838) или Windows 8. x, установите пакет средств разработки программного обеспечения (SDK) для Windows 8. x, чтобы получить \_1SDKLayers.dll D3D11.</span><span class="sxs-lookup"><span data-stu-id="ee330-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="ee330-125">В Windows 10 для создания устройства, поддерживающего уровень отладки, включите необязательный компонент "графические средства".</span><span class="sxs-lookup"><span data-stu-id="ee330-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="ee330-126">Перейдите на панель "Параметры" в разделе "система", "приложения & компоненты", "Управление дополнительными компонентами", "добавить компонент" и найдите "графические инструменты".</span><span class="sxs-lookup"><span data-stu-id="ee330-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="ee330-127">Сведения об удаленной отладке приложений DirectX см. в разделе [Отладка приложений DirectX удаленно](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="ee330-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="ee330-128">Кроме того, флаг отладки можно включить или отключить с помощью [панели управления DirectX](/previous-versions//bb219725(v=vs.85)) , входящей в состав пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="ee330-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="ee330-129">Когда уровень отладки перечисляет утечки памяти, он выводит список указателей на объектные интерфейсы и их понятные имена.</span><span class="sxs-lookup"><span data-stu-id="ee330-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="ee330-130">Понятное имя по умолчанию — безымянное &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="ee330-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="ee330-131">Понятное имя можно задать с помощью метода [**ID3D11DeviceChild:: сетприватедата**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) и идентификатора GUID **вкпдид \_ D3DDebugObjectName** , который находится в D3Dcommon. h.</span><span class="sxs-lookup"><span data-stu-id="ee330-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="ee330-132">Например, чтобы присвоить имя Птекстуре имя Сдклайер mytexture.jpg, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="ee330-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="ee330-133">Как правило, следует компилировать эти вызовы из рабочей версии.</span><span class="sxs-lookup"><span data-stu-id="ee330-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee330-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ee330-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee330-135">Устройства</span><span class="sxs-lookup"><span data-stu-id="ee330-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 
---
description: Приложения могут запрашивать оборудование для обнаружения поддерживаемых типов устройств Direct3D. В этом разделе содержатся сведения о главных задачах, связанных с перечислением видеоадаптеров и выбором устройств Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Выбор устройства (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538225"
---
# <a name="selecting-a-device-direct3d-9"></a><span data-ttu-id="b8edd-104">Выбор устройства (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8edd-104">Selecting a Device (Direct3D 9)</span></span>

<span data-ttu-id="b8edd-105">Приложения могут запрашивать оборудование для обнаружения поддерживаемых типов устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8edd-105">Applications can query hardware to detect the supported Direct3D device types.</span></span> <span data-ttu-id="b8edd-106">В этом разделе содержатся сведения о главных задачах, связанных с перечислением видеоадаптеров и выбором устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8edd-106">This section contains information about the primary tasks involved in enumerating display adapters and selecting Direct3D devices.</span></span>

<span data-ttu-id="b8edd-107">Приложение должно выполнить ряд задач, чтобы выбрать подходящее устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b8edd-107">An application must perform a series of tasks to select an appropriate Direct3D device.</span></span> <span data-ttu-id="b8edd-108">Обратите внимание, что следующие шаги предназначены для полноэкранного приложения. в большинстве случаев оконное приложение может пропускать большинство этих шагов.</span><span class="sxs-lookup"><span data-stu-id="b8edd-108">Note that the following steps are intended for a full-screen application and that, in most cases, a windowed application can skip most of these steps.</span></span>

1.  <span data-ttu-id="b8edd-109">Изначально приложение должно перечислить видеоадаптеры в системе.</span><span class="sxs-lookup"><span data-stu-id="b8edd-109">Initially, the application must enumerate the display adapters on the system.</span></span> <span data-ttu-id="b8edd-110">Адаптер — это физический компонент оборудования.</span><span class="sxs-lookup"><span data-stu-id="b8edd-110">An adapter is a physical piece of hardware.</span></span> <span data-ttu-id="b8edd-111">Обратите внимание, что графическая карта может содержать больше одного адаптера, как в случае с двумя наконечниками.</span><span class="sxs-lookup"><span data-stu-id="b8edd-111">Note that the graphics card might contain more than a single adapter, as is the case with a dual-headed display.</span></span> <span data-ttu-id="b8edd-112">Приложения, не имеющие поддержки нескольких мониторов, могут проигнорировать этот шаг и передать D3DADAPTER \_ по умолчанию методу [**IDirect3D9:: енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="b8edd-112">Applications that are not concerned with multi-monitor support can disregard this step, and pass D3DADAPTER\_DEFAULT to the [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) method in step 2.</span></span>
2.  <span data-ttu-id="b8edd-113">Для каждого адаптера приложение перечисляет поддерживаемые режимы экрана, вызывая [**IDirect3D9:: енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="b8edd-113">For each adapter, the application enumerates the supported display modes by calling [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>
3.  <span data-ttu-id="b8edd-114">При необходимости приложение проверяет наличие аппаратного ускорения в каждом перечислимом режиме путем вызова [**IDirect3D9:: чеккдевицетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b8edd-114">If required, the application checks for the presence of hardware acceleration in each enumerated display mode by calling [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), as shown in the following code example.</span></span> <span data-ttu-id="b8edd-115">Обратите внимание, что это только одно из возможных применений для **IDirect3D9:: чеккдевицетипе**; Дополнительные сведения см. в разделе [Определение аппаратной поддержки (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="b8edd-115">Note that this is only one of the possible uses for **IDirect3D9::CheckDeviceType**; for details, see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  <span data-ttu-id="b8edd-116">Приложение проверяет требуемый уровень функциональности для устройства на этом адаптере, вызывая метод [**IDirect3D9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="b8edd-116">The application checks for the desired level of functionality for the device on this adapter by calling the [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) method.</span></span> <span data-ttu-id="b8edd-117">Возможность, возвращаемая этим методом, гарантированно будет постоянной для устройства во всех режимах экрана, проверенных с помощью [**IDirect3D9:: чеккдевицетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span><span class="sxs-lookup"><span data-stu-id="b8edd-117">The capability returned by this method is guaranteed to be constant for a device across all display modes, verified by [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span></span>
5.  <span data-ttu-id="b8edd-118">Устройства всегда могут быть отображены на поверхности формата перечисленного режима отображения, поддерживаемого устройством.</span><span class="sxs-lookup"><span data-stu-id="b8edd-118">Devices can always render to surfaces of the format of an enumerated display mode that is supported by the device.</span></span> <span data-ttu-id="b8edd-119">Если требуется, чтобы приложение отображалось на поверхности другого формата, оно может вызвать [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="b8edd-119">If the application is required to render to a surface of a different format, it can call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span> <span data-ttu-id="b8edd-120">Если устройство может подготовиться к просмотру в формате, то гарантируется, что все возможности, возвращаемые [**IDirect3D9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) , применимы.</span><span class="sxs-lookup"><span data-stu-id="b8edd-120">If the device can render to the format, then it is guaranteed that all capabilities returned by [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) are applicable.</span></span>
6.  <span data-ttu-id="b8edd-121">Наконец, приложение может определить, поддерживаются ли Многовыборочные приемы, такие как сглаживание с полными сценами, для формата отрисовки с помощью метода [**IDirect3D9:: чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) .</span><span class="sxs-lookup"><span data-stu-id="b8edd-121">Lastly, the application can determine if multisampling techniques, such as full-scene antialiasing, are supported for a render format by using the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method.</span></span>

<span data-ttu-id="b8edd-122">После выполнения описанных выше действий приложение должно иметь список режимов экрана, в которых он может действовать.</span><span class="sxs-lookup"><span data-stu-id="b8edd-122">After completing the preceding steps, the application should have a list of display modes in which it can operate.</span></span> <span data-ttu-id="b8edd-123">Последним шагом является проверка наличия достаточного объема доступной для устройства памяти для размещения необходимого количества буферов и сглаживания.</span><span class="sxs-lookup"><span data-stu-id="b8edd-123">The final step is to verify that enough device-accessible memory is available to accommodate the required number of buffers and antialiasing.</span></span> <span data-ttu-id="b8edd-124">Этот тест необходим, так как использование памяти для сочетания режима и многопримерной комбинации невозможно предсказать без проверки.</span><span class="sxs-lookup"><span data-stu-id="b8edd-124">This test is necessary because the memory consumption for the mode and multisample combination is impossible to predict without verifying it.</span></span> <span data-ttu-id="b8edd-125">Более того, некоторые архитектуры видеоадаптеров могут не иметь постоянного объема памяти, доступной для устройств.</span><span class="sxs-lookup"><span data-stu-id="b8edd-125">Moreover, some display adapter architectures might not have a constant amount of device-accessible memory.</span></span> <span data-ttu-id="b8edd-126">Это означает, что приложение должно иметь возможность сообщать о сбоях нехватки памяти при переходе в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="b8edd-126">This means that an application should be able to report out-of-video-memory failures when going into full-screen mode.</span></span> <span data-ttu-id="b8edd-127">Как правило, приложение должно удалить полноэкранный режим из списка режимов, которые он предлагает пользователю, или попытаться использовать меньше памяти, уменьшая количество задних буферов или используя менее сложный метод множественной выборки.</span><span class="sxs-lookup"><span data-stu-id="b8edd-127">Typically, an application should remove full-screen mode from the list of modes that it offers to a user, or it should attempt to consume less memory by reducing the number of back buffers or by using a less complex multisampling technique.</span></span>

<span data-ttu-id="b8edd-128">Оконное приложение выполняет аналогичный набор задач.</span><span class="sxs-lookup"><span data-stu-id="b8edd-128">A windowed application performs a similar set of tasks.</span></span>

1.  <span data-ttu-id="b8edd-129">Он определяет прямоугольник рабочего стола, покрываемый клиентской областью окна.</span><span class="sxs-lookup"><span data-stu-id="b8edd-129">It determines the desktop rectangle covered by the client area of the window.</span></span>
2.  <span data-ttu-id="b8edd-130">Он перечисляет адаптеры, ищут адаптер, монитор которого охватывает клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="b8edd-130">It enumerates adapters, looking for the adapter whose monitor covers the client area.</span></span> <span data-ttu-id="b8edd-131">Если клиентская область принадлежит более чем одному адаптеру, то приложение может выбрать один из них для каждого адаптера или для одного адаптера и передать пикселы с одного устройства на другое в презентации.</span><span class="sxs-lookup"><span data-stu-id="b8edd-131">If the client area is owned by more than one adapter, then the application can choose to drive each adapter independently, or to drive a single adapter and have Direct3D transfer pixels from one device to another at presentation.</span></span> <span data-ttu-id="b8edd-132">Приложение также может проигнорировать два предыдущих шага и использовать адаптер D3DADAPTER \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8edd-132">The application can also disregard two preceding steps and use the D3DADAPTER\_DEFAULT adapter.</span></span> <span data-ttu-id="b8edd-133">Обратите внимание, что это может привести к более медленной работе, когда окно помещается на дополнительный монитор.</span><span class="sxs-lookup"><span data-stu-id="b8edd-133">Note that this might result in slower operation when the window is placed on a secondary monitor.</span></span>
3.  <span data-ttu-id="b8edd-134">Приложение должно вызывать [**IDirect3D9:: чеккдевицетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) , чтобы определить, может ли устройство поддерживать отрисовку в обратном буфере указанного формата в режиме рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b8edd-134">The application should call [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) to determine if the device can support rendering to a back buffer of the specified format while in desktop mode.</span></span> <span data-ttu-id="b8edd-135">[**IDirect3D9:: жетадаптердисплаймоде**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) можно использовать для определения формата отображения рабочего стола, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b8edd-135">[**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) can be used to determine the desktop display format, as shown in the following code example.</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b8edd-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b8edd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8edd-137">Устройства Direct3D</span><span class="sxs-lookup"><span data-stu-id="b8edd-137">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 

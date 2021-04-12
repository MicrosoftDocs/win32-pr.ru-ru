---
description: диспетчер устройств Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: диспетчер устройств Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342505"
---
# <a name="direct3d-device-manager"></a><span data-ttu-id="fbe29-103">диспетчер устройств Direct3D</span><span class="sxs-lookup"><span data-stu-id="fbe29-103">Direct3D Device Manager</span></span>

<span data-ttu-id="fbe29-104">Диспетчер устройств Microsoft Direct3D позволяет нескольким объектам совместно использовать одно и то же устройство Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="fbe29-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="fbe29-105">Один объект выступает в качестве владельца устройства Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="fbe29-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="fbe29-106">Чтобы предоставить общий доступ к устройству, владелец устройства создает диспетчер устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fbe29-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="fbe29-107">Другие объекты могут получить указатель на диспетчер устройств от владельца устройства, а затем использовать диспетчер устройств для получения указателя на устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fbe29-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="fbe29-108">Любой объект, использующий устройство, удерживает монопольную блокировку, которая предотвращает одновременное использование устройства другими объектами.</span><span class="sxs-lookup"><span data-stu-id="fbe29-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="fbe29-109">Direct3D диспетчер устройств поддерживает только устройства Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="fbe29-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="fbe29-110">Он не поддерживает устройства DXGI.</span><span class="sxs-lookup"><span data-stu-id="fbe29-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="fbe29-111">Чтобы создать диспетчер устройств Direct3D, вызовите [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="fbe29-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="fbe29-112">Эта функция возвращает указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) диспетчера устройств, а также маркер сброса.</span><span class="sxs-lookup"><span data-stu-id="fbe29-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="fbe29-113">Маркер сброса позволяет владельцу устройства Direct3D устанавливать (и сбрасывать) устройство в диспетчере устройств.</span><span class="sxs-lookup"><span data-stu-id="fbe29-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="fbe29-114">Чтобы инициализировать диспетчер устройств, вызовите метод [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="fbe29-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="fbe29-115">Передайте указатель на устройство Direct3D, а также маркер сброса.</span><span class="sxs-lookup"><span data-stu-id="fbe29-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="fbe29-116">В следующем коде показано, как создать и инициализировать диспетчер устройств.</span><span class="sxs-lookup"><span data-stu-id="fbe29-116">The following code shows how to create and initialize the device manager.</span></span>


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



<span data-ttu-id="fbe29-117">Владелец устройства должен предоставить другим объектам возможность получить указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="fbe29-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="fbe29-118">Стандартный механизм заключается в реализации интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="fbe29-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="fbe29-119">Идентификатор GUID службы — это \_ Служба ускорения видео (MR) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fbe29-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="fbe29-120">Чтобы предоставить общий доступ к устройству нескольким объектам, каждый объект (включая владельца устройства) должен получить доступ к устройству через диспетчер устройств, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fbe29-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="fbe29-121">Вызовите [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="fbe29-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="fbe29-122">Чтобы использовать устройство, вызовите [**IDirect3DDeviceManager9:: локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) и передайте его в маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="fbe29-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="fbe29-123">Метод возвращает указатель на интерфейс **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="fbe29-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="fbe29-124">Метод может быть вызван в блокирующем режиме или в режиме без блокировки, в зависимости от значения параметра *фблокк* .</span><span class="sxs-lookup"><span data-stu-id="fbe29-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="fbe29-125">По завершении использования устройства вызовите [**IDirect3DDeviceManager9:: унлоккдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="fbe29-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="fbe29-126">Этот метод делает устройство доступным для других объектов.</span><span class="sxs-lookup"><span data-stu-id="fbe29-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="fbe29-127">Перед выходом вызовите метод [**IDirect3DDeviceManager9:: клоседевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) , чтобы закрыть маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="fbe29-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="fbe29-128">Блокировка устройства должна удерживаться только при использовании устройства, так как удержание блокировки устройства не позволяет другим объектам использовать устройство.</span><span class="sxs-lookup"><span data-stu-id="fbe29-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="fbe29-129">Владелец устройства может переключиться на другое устройство в любое время, вызвав [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), как правило, из-за потери исходного устройства.</span><span class="sxs-lookup"><span data-stu-id="fbe29-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="fbe29-130">Потери устройств могут возникать по различным причинам, включая изменения в разрешении монитора, действия управления питанием, блокировку и разблокирование компьютера и т. д.</span><span class="sxs-lookup"><span data-stu-id="fbe29-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="fbe29-131">Дополнительные сведения см. в документации по Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fbe29-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="fbe29-132">Метод [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) делает недействительными все дескрипторы устройств, которые были открыты ранее.</span><span class="sxs-lookup"><span data-stu-id="fbe29-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="fbe29-133">Если недопустимый маркер устройства, метод [**локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) возвращает **\_ \_ новое \_ видео- \_ устройство DXVA2 E**.</span><span class="sxs-lookup"><span data-stu-id="fbe29-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="fbe29-134">Если это происходит, закройте этот обработчик и снова вызовите [**опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить новый маркер устройства, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="fbe29-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="fbe29-135">В следующем примере показано, как открыть обработчик устройства и заблокировать его.</span><span class="sxs-lookup"><span data-stu-id="fbe29-135">The following example shows how to open a device handle and lock the device.</span></span>


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fbe29-136">См. также</span><span class="sxs-lookup"><span data-stu-id="fbe29-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbe29-137">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="fbe29-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 




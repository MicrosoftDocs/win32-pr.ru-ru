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
# <a name="direct3d-device-manager"></a>диспетчер устройств Direct3D

Диспетчер устройств Microsoft Direct3D позволяет нескольким объектам совместно использовать одно и то же устройство Microsoft Direct3D 9. Один объект выступает в качестве владельца устройства Direct3D 9. Чтобы предоставить общий доступ к устройству, владелец устройства создает диспетчер устройств Direct3D. Другие объекты могут получить указатель на диспетчер устройств от владельца устройства, а затем использовать диспетчер устройств для получения указателя на устройство Direct3D. Любой объект, использующий устройство, удерживает монопольную блокировку, которая предотвращает одновременное использование устройства другими объектами.

> [!Note]  
> Direct3D диспетчер устройств поддерживает только устройства Direct3D 9. Он не поддерживает устройства DXGI.

 

Чтобы создать диспетчер устройств Direct3D, вызовите [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Эта функция возвращает указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) диспетчера устройств, а также маркер сброса. Маркер сброса позволяет владельцу устройства Direct3D устанавливать (и сбрасывать) устройство в диспетчере устройств. Чтобы инициализировать диспетчер устройств, вызовите метод [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Передайте указатель на устройство Direct3D, а также маркер сброса.

В следующем коде показано, как создать и инициализировать диспетчер устройств.


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



Владелец устройства должен предоставить другим объектам возможность получить указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Стандартный механизм заключается в реализации интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Идентификатор GUID службы — это \_ Служба ускорения видео (MR) \_ \_ .

Чтобы предоставить общий доступ к устройству нескольким объектам, каждый объект (включая владельца устройства) должен получить доступ к устройству через диспетчер устройств, как показано ниже.

1.  Вызовите [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить маркер устройства.
2.  Чтобы использовать устройство, вызовите [**IDirect3DDeviceManager9:: локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) и передайте его в маркер устройства. Метод возвращает указатель на интерфейс **IDirect3DDevice9** . Метод может быть вызван в блокирующем режиме или в режиме без блокировки, в зависимости от значения параметра *фблокк* .
3.  По завершении использования устройства вызовите [**IDirect3DDeviceManager9:: унлоккдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Этот метод делает устройство доступным для других объектов.
4.  Перед выходом вызовите метод [**IDirect3DDeviceManager9:: клоседевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) , чтобы закрыть маркер устройства.

Блокировка устройства должна удерживаться только при использовании устройства, так как удержание блокировки устройства не позволяет другим объектам использовать устройство.

Владелец устройства может переключиться на другое устройство в любое время, вызвав [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), как правило, из-за потери исходного устройства. Потери устройств могут возникать по различным причинам, включая изменения в разрешении монитора, действия управления питанием, блокировку и разблокирование компьютера и т. д. Дополнительные сведения см. в документации по Direct3D.

Метод [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) делает недействительными все дескрипторы устройств, которые были открыты ранее. Если недопустимый маркер устройства, метод [**локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) возвращает **\_ \_ новое \_ видео- \_ устройство DXVA2 E**. Если это происходит, закройте этот обработчик и снова вызовите [**опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить новый маркер устройства, как показано в следующем коде.

В следующем примере показано, как открыть обработчик устройства и заблокировать его.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ускорение видео DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 




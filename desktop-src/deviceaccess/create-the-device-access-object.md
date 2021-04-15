---
title: Реализация объекта доступа к устройству
description: В этом разделе объясняется, как создать объект доступа к устройству и использовать его для доступа к устройству.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 60bd634f72b29bb6520223a7933b22a396f99723
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488487"
---
# <a name="implement-the-device-access-object"></a>Реализация объекта доступа к устройству

В этом разделе объясняется, как создать объект доступа к устройству и использовать его для доступа к устройству. Экземпляр класса реализует интерфейсы [**идевицеиоконтрол**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) и [**икреатедевицеакцессасинк**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) .

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1

Чтобы создать экземпляр объекта доступа к устройству, необходимо сначала вызвать функцию [**креатедевицеакцессинстанце**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) . Если **креатедевицеакцессинстанце** завершается, можно вызвать метод [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) , чтобы дождаться завершения асинхронной операции. Если **Ожидание** завершилось, можно получить объект [**идевицеиоконтрол**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (или соответствующую ошибку) из метода [**result**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) .

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &amp;pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&amp;m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a>Шаг 2

Это пример вызова метода **девицеиоконтролсинк** .


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &amp;sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a>Комментарии

Можно также асинхронно отправить запрос IOCTL с помощью метода [**девицеиоконтроласинк**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) . В этом случае необходимо реализовать интерфейс [**идевицерекуесткомплетионкаллбакк**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) .

## <a name="related-topics"></a>См. также

[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)

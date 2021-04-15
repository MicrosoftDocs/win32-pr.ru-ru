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
# <a name="implement-the-device-access-object"></a><span data-ttu-id="03da9-103">Реализация объекта доступа к устройству</span><span class="sxs-lookup"><span data-stu-id="03da9-103">Implement the Device Access Object</span></span>

<span data-ttu-id="03da9-104">В этом разделе объясняется, как создать объект доступа к устройству и использовать его для доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="03da9-104">This topic explains how to instantiate the device access object and use it to access a device.</span></span> <span data-ttu-id="03da9-105">Экземпляр класса реализует интерфейсы [**идевицеиоконтрол**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) и [**икреатедевицеакцессасинк**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) .</span><span class="sxs-lookup"><span data-stu-id="03da9-105">The instantiated class implements the [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) and [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interfaces.</span></span>

## <a name="instructions"></a><span data-ttu-id="03da9-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="03da9-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="03da9-107">Шаг 1</span><span class="sxs-lookup"><span data-stu-id="03da9-107">Step 1</span></span>

<span data-ttu-id="03da9-108">Чтобы создать экземпляр объекта доступа к устройству, необходимо сначала вызвать функцию [**креатедевицеакцессинстанце**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) .</span><span class="sxs-lookup"><span data-stu-id="03da9-108">To instantiate the device access object, you must first call the [**CreateDeviceAccessInstance**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) function.</span></span> <span data-ttu-id="03da9-109">Если **креатедевицеакцессинстанце** завершается, можно вызвать метод [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) , чтобы дождаться завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="03da9-109">If **CreateDeviceAccessInstance** succeeds, you can then call the [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) method to wait for the asynchronous operation to finish.</span></span> <span data-ttu-id="03da9-110">Если **Ожидание** завершилось, можно получить объект [**идевицеиоконтрол**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (или соответствующую ошибку) из метода [**result**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) .</span><span class="sxs-lookup"><span data-stu-id="03da9-110">If **Wait** succeeds, you can retrieve an [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) object (or the appropriate error) from the [**GetResult**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) method.</span></span>

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



### <a name="step-2"></a><span data-ttu-id="03da9-111">Шаг 2</span><span class="sxs-lookup"><span data-stu-id="03da9-111">Step 2</span></span>

<span data-ttu-id="03da9-112">Это пример вызова метода **девицеиоконтролсинк** .</span><span class="sxs-lookup"><span data-stu-id="03da9-112">This is an example of a call to the **DeviceIoControlSync** method.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="03da9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03da9-113">Remarks</span></span>

<span data-ttu-id="03da9-114">Можно также асинхронно отправить запрос IOCTL с помощью метода [**девицеиоконтроласинк**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) .</span><span class="sxs-lookup"><span data-stu-id="03da9-114">You can also send an IOCTL asynchronously by using the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) method.</span></span> <span data-ttu-id="03da9-115">В этом случае необходимо реализовать интерфейс [**идевицерекуесткомплетионкаллбакк**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) .</span><span class="sxs-lookup"><span data-stu-id="03da9-115">In that case, you must implement the [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03da9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="03da9-116">Related topics</span></span>

<span data-ttu-id="03da9-117">[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="03da9-117">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>

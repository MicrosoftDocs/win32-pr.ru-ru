---
title: Обработка защищенного содержимого в приложении
description: Обработка защищенного содержимого в приложении
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Диспетчер устройств Windows Media, сертификаты
- Диспетчер устройств, сертификаты
- рекомендации по программированию, сертификаты
- Классические приложения, сертификаты
- Создание приложений диспетчер устройств Windows Media, сертификаты
- certificates
- Диспетчер устройств Windows Media, содержимое, защищенное с использованием DRM
- Диспетчер устройств, содержимое, защищенное с использованием DRM
- Путеводитель по программированию, содержимое, защищенное с использованием DRM
- Классические приложения, содержимое, защищенное с использованием DRM
- Создание приложений Windows Media диспетчер устройств, содержимое, защищенное с использованием DRM
- Содержимое, защищенное DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691607"
---
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="5f285-115">Обработка защищенного содержимого в приложении</span><span class="sxs-lookup"><span data-stu-id="5f285-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="5f285-116">\[Компонент Windows Media DRM является устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="5f285-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="5f285-117">Вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="5f285-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="5f285-118">Приложение должно иметь сертификат для перемещения, чтобы иметь возможность обрабатывать содержимое, защищенное с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="5f285-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="5f285-119">Сведения о том, как получить этот сертификат, см. в разделе [средства для разработки](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="5f285-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="5f285-120">Для обработки незащищенного содержимого можно использовать фиктивный сертификат, как описано в разделе [Проверка подлинности приложения](authenticating-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="5f285-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="5f285-121">Перед использованием устройства приложение должно определить, поддерживает ли устройство Windows Media DRM 10 для переносных устройств, и, если это так, что компоненты DRM являются актуальными.</span><span class="sxs-lookup"><span data-stu-id="5f285-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="5f285-122">(Текущее значение означает, что безопасное время и устройство настроены правильно.) Если устройство не поддерживает эту версию DRM или не может быть Обновлено, вы по-прежнему можете отправить файлы на устройство, но они могут не воспроизводиться в зависимости от версии лицензии.</span><span class="sxs-lookup"><span data-stu-id="5f285-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="5f285-123">Индивидуальность устройств в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f285-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="5f285-124">Если приложение будет ссылаться на методы пакета SDK Windows Media Format, необходимо будет связать библиотеку формата Windows Media Вмстубдрм. lib.</span><span class="sxs-lookup"><span data-stu-id="5f285-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="5f285-125">Дополнительные сведения о вызове методов формата Windows Media для содержимого, защищенного с помощью DRM, см. в разделе "Включение поддержки DRM" в документации по пакету SDK для Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5f285-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="5f285-126">Обратите внимание, что существует проблема связывания с Мссачлп. lib и Вмстубдрм. lib.</span><span class="sxs-lookup"><span data-stu-id="5f285-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="5f285-127">Это описано в [статье 890079 базы знаний MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span><span class="sxs-lookup"><span data-stu-id="5f285-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="5f285-128">В следующем примере кода C++ определяется, является ли устройство устройством Windows Media DRM 10, и, если это так, что его часы актуальны.</span><span class="sxs-lookup"><span data-stu-id="5f285-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



<span data-ttu-id="5f285-129">Если устройство поддерживает Windows Media DRM 10 для переносных устройств и должно быть Обновлено (т. е. Если значение *Status* в предыдущем примере не просто вмдм \_ Device \_ исвмдрм), приложение должно вызвать [**ивмдрмдевицеапп:: аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать значение *Status* , чтобы выполнить необходимые обновления.</span><span class="sxs-lookup"><span data-stu-id="5f285-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="5f285-130">Настольный компьютер должен быть подключен к Интернету.</span><span class="sxs-lookup"><span data-stu-id="5f285-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="5f285-131">Следующая функция примера C++ пытается обновить устройство DRM.</span><span class="sxs-lookup"><span data-stu-id="5f285-131">The following C++ example function attempts to update a DRM device.</span></span>


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5f285-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5f285-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f285-133">**Создание приложения диспетчер устройств Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5f285-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="5f285-134">**Обработка защищенного содержимого**</span><span class="sxs-lookup"><span data-stu-id="5f285-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 
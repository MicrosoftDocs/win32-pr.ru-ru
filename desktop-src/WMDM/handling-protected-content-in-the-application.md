---
title: Обработка защищенного содержимого в приложении
description: Обработка защищенного содержимого в приложении
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Диспетчер устройств мультимедиа, сертификаты
- Диспетчер устройств, сертификаты
- рекомендации по программированию, сертификаты
- Классические приложения, сертификаты
- создание Windows мультимедиа диспетчер устройств приложений, сертификаты
- certificates
- Windows Диспетчер устройств мультимедиа, содержимое, защищенное с использованием DRM
- Диспетчер устройств, содержимое, защищенное с использованием DRM
- Путеводитель по программированию, содержимое, защищенное с использованием DRM
- Классические приложения, содержимое, защищенное с использованием DRM
- создание Windows мультимедиа диспетчер устройств приложений, содержимое, защищенное с использованием DRM
- Содержимое, защищенное DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0befd0eb9fe2fecf06235b0b9424776ed25f3b1c411439cac5ecdfa71910d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957374"
---
# <a name="handling-protected-content-in-the-application"></a>Обработка защищенного содержимого в приложении

\[функция DRM Windows мультимедиа является устаревшей и не должна использоваться. вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Приложение должно иметь сертификат для перемещения, чтобы иметь возможность обрабатывать содержимое, защищенное с помощью DRM. Сведения о том, как получить этот сертификат, см. в разделе [средства для разработки](tools-for-development.md). Для обработки незащищенного содержимого можно использовать фиктивный сертификат, как описано в разделе [Проверка подлинности приложения](authenticating-the-application.md).

перед использованием устройства приложение должно определить, поддерживает ли устройство Windows Media DRM 10 для портативных устройств, и, если это так, что компоненты DRM являются актуальными. (Текущее значение означает, что безопасное время и устройство настроены правильно.) Если устройство не поддерживает эту версию DRM или не может быть Обновлено, вы по-прежнему можете отправить файлы на устройство, но они могут не воспроизводиться в зависимости от версии лицензии.

> [!Note]  
> Индивидуальность устройств в настоящее время не поддерживается.

 

если приложение будет связываться с Windows методами пакета SDK формата мультимедиа, необходимо будет создать ссылку на Windows библиотеку формата мультимедиа вмстубдрм. lib. дополнительные сведения о вызове методов Windowsного формата мультимедиа для содержимого, защищенного с помощью drm, см. в разделе "включение поддержки drm" в документации пакета SDK для Windows Media Format. Обратите внимание, что существует проблема связывания с Мссачлп. lib и Вмстубдрм. lib. Это описано в [статье 890079 базы знаний MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

в следующем примере кода C++ определяется, является ли устройство устройством Windows Media DRM 10, и, если это так, что его часы актуальны.

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



если устройство поддерживает Windows Media DRM 10 для переносных устройств и должно быть обновлено (то есть если значение *status* в предыдущем примере не просто вмдм \_ device \_ исвмдрм), приложение должно вызвать [**ивмдрмдевицеапп:: аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать значение *status* , чтобы выполнить необходимые обновления. Настольный компьютер должен быть подключен к Интернету.

Следующая функция примера C++ пытается обновить устройство DRM.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**создание Windows мультимедиа диспетчер устройств приложение**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Обработка защищенного содержимого**](handling-protected-content.md)
</dt> </dl>

 

 
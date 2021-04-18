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
# <a name="handling-protected-content-in-the-application"></a>Обработка защищенного содержимого в приложении

\[Компонент Windows Media DRM является устаревшим и не должен использоваться. Вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Приложение должно иметь сертификат для перемещения, чтобы иметь возможность обрабатывать содержимое, защищенное с помощью DRM. Сведения о том, как получить этот сертификат, см. в разделе [средства для разработки](tools-for-development.md). Для обработки незащищенного содержимого можно использовать фиктивный сертификат, как описано в разделе [Проверка подлинности приложения](authenticating-the-application.md).

Перед использованием устройства приложение должно определить, поддерживает ли устройство Windows Media DRM 10 для переносных устройств, и, если это так, что компоненты DRM являются актуальными. (Текущее значение означает, что безопасное время и устройство настроены правильно.) Если устройство не поддерживает эту версию DRM или не может быть Обновлено, вы по-прежнему можете отправить файлы на устройство, но они могут не воспроизводиться в зависимости от версии лицензии.

> [!Note]  
> Индивидуальность устройств в настоящее время не поддерживается.

 

Если приложение будет ссылаться на методы пакета SDK Windows Media Format, необходимо будет связать библиотеку формата Windows Media Вмстубдрм. lib. Дополнительные сведения о вызове методов формата Windows Media для содержимого, защищенного с помощью DRM, см. в разделе "Включение поддержки DRM" в документации по пакету SDK для Windows Media Format. Обратите внимание, что существует проблема связывания с Мссачлп. lib и Вмстубдрм. lib. Это описано в [статье 890079 базы знаний MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

В следующем примере кода C++ определяется, является ли устройство устройством Windows Media DRM 10, и, если это так, что его часы актуальны.

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



Если устройство поддерживает Windows Media DRM 10 для переносных устройств и должно быть Обновлено (т. е. Если значение *Status* в предыдущем примере не просто вмдм \_ Device \_ исвмдрм), приложение должно вызвать [**ивмдрмдевицеапп:: аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать значение *Status* , чтобы выполнить необходимые обновления. Настольный компьютер должен быть подключен к Интернету.

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание приложения диспетчер устройств Windows Media**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Обработка защищенного содержимого**](handling-protected-content.md)
</dt> </dl>

 

 
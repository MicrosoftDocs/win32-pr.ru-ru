---
description: Требования к приложениям DRM-Enabled Windows Media
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Требования к приложениям DRM-Enabled Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713295"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Требования к приложениям DRM-Enabled Windows Media

Чтобы создать приложение с поддержкой цифровых Rights Management Windows Media (DRM), необходимо иметь заголовки и библиотеки, описанные в разделе [Общие требования для разработки приложений](general-requirements-for-application-development.md) этого документа. Кроме того, при открытии устройства приложению потребуется предоставить дополнительные свойства в сведениях о клиенте.

В следующей таблице описаны два дополнительных свойства, необходимые для включения передачи содержимого, защищенного с помощью DRM Windows Media.



| Свойство                                      | Описание                              |
|-----------------------------------------------|------------------------------------------|
| \_ \_ \_ \_ закрытый ключ клиентского приложения WPD с цифровыми правами \_ | Указывает закрытый ключ приложения. |
| \_сертификат приложения WPD клиента для \_ WMDRM \_ \_  | Указывает сертификат приложения. |



 

Эти свойства должны быть заданы в клиентской информации приложения при открытии устройства с помощью метода [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) . При предоставлении этих свойств API-интерфейс WPD позволяет передавать защищенное содержимое. Если приложение предоставил сертификат и закрытый ключ, API создаст защищенный канал для передачи защищенного WMDRM-содержимого на устройство.

Сведения о создании и распространении приложений Windows, которые поддерживают Windows Media DRM, см. в следующем разделе [Лицензирование приложений на основе Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .

## <a name="transferring-content"></a>Передача содержимого

Чтобы переместить защищенное WMDRM содержимое, используйте [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Этот метод можно использовать как для защищенного, так и для открытого содержимого без дополнительных параметров. API-интерфейс WPD автоматически выбирает защищенный или сброшенный канал в зависимости от того, является ли содержимое защищенным или открытым. Он взаимодействует с поставщиком безопасного содержимого WMDRM для обработки лицензий WMDRM.

## <a name="transferring-known-clear-content"></a>Передача известного открытого содержимого

Если вы включили приложение для обработки защищенного содержимого, но знаете, что конкретный файл не защищен, вы можете сообщить WPD, что он пропускает обработку DRM, установив **\_ параметр API \_ - \_ \_ \_ \_ интерфейса WPD** в поле входные **ипортабледевицевалуес** при вызове [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) для очистки содержимого.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Доступ к операциям отслеживания использования с помощью Ивмдрмдевицеапп

Средство WPD предоставляет механизм доступа к API **ивмдрмдевицеапп** для обновлений лицензий и получения данных контроля использования. Чтобы получить доступ к этому API через WPD, вызовите **QueryInterface** для **IID \_ ивмдрмдевицеапп** из **IStream** , возвращенного из [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Этот экземпляр **ивмдрмдевицеапп** связан с подключением **ипортабледевице** к устройству, совместимому с WMDRM, а не с конкретным содержимым, в котором был получен объект **IStream** . WPD внутренне заключает в оболочку API отслеживания использования и делает его доступным для вашего приложения. Для параметра Ивмдмдевице в приложении следует \_ использовать \_ \_ \_ константу PTR для устройства  WPD вмдрмдевицеапп \* .

Это показано в следующем фрагменте кода.


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



Также применяется тот же самый предварительный компонент с закрытым ключом приложения и сертификатом. Если ключ или сертификат недействительны или не удается инициализировать систему WMDRM, вызов **куеринферфаце** завершится ошибкой.

Приведенный выше метод получения интерфейса **ивмдрмдевицеапп** из указателя **IStream** является просто удобным, если приложение уже выполняет предыдущий защищенный перенос содержимого, прежде чем продолжать выполнение операций отслеживания и синхронизации лицензий.

Наша рекомендация для большинства приложений, которым требуется доступ к **ивмдрмдевицеапп** , — это инициализация **ивмдрмдевицеапп** напрямую, так как это не требует от приложения передавать защищенное содержимое или хранить их в интерфейсах перемещения, чтобы обеспечить отслеживание устройств и синхронизацию лицензий. Для этого метода потребуется использование интерфейсов API Windows Media диспетчер устройств (ВМДМ). Дополнительные сведения и примеры кода см. в техническом документе о [приложении WPD](../windows-portable-devices.md) на сайте вхдк.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Портативные устройства Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 

---
description: Интерфейс устройства может быть описан с помощью значения GUID. Портативные устройства Windows определяют следующий интерфейс устройства.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: Идентификаторы GUID интерфейса устройства (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704511"
---
# <a name="device-interface-guids"></a>Идентификаторы GUID интерфейса устройства

Интерфейс устройства может быть описан с помощью значения **GUID** . Портативные устройства Windows определяют следующий интерфейс устройства.



| Константа                                                                                                                                                                                                        | Описание                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ девинтерфаце \_ WPD**</dt> </dl>                          | Определяет устройства, которые отображаются в стандартном перечислении WPD. Любое устройство, которое регистрирует этот GUID интерфейса, будет перечисляться, когда приложение вызывает метод [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) GetEnumerator.<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ девинтерфаце \_ WPD \_ Private**</dt> </dl> | Определяет устройства, которые не будут отображаться в стандартном перечислении WPD. Любое устройство, которое регистрирует этот GUID интерфейса, будет перечисляться только в том случае, если приложение вызывает метод [**ипортабледевицеманажер:: жетприватедевицес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ девинтерфаце \_ WPD \_ Service**</dt> </dl> | В Windows 7 приложения могут перечислять все службы устройств WPD, вызывая [**ипортабледевицесервицеманажер:: жетдевицесервицес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) и используя этот класс интерфейса в качестве идентификатора GUID типа службы.<br/>                                   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по программированию](programming-reference.md)
</dt> </dl>

 

 





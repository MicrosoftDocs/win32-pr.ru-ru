---
description: 'Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для событий службы устройства. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетевентаттрибутес.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Атрибуты событий (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694430"
---
# <a name="event-attributes-portabledeviceh"></a>Атрибуты событий (Портабледевице. h)

Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для событий службы устройства. Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетевентаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| attribute                             | VarType         | Описание                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ имя атрибута события \_ WPD**       | **VT \_ LPWSTR**  | Строка, указывающая понятное для сценария имя события. Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ". |
| **\_ \_ параметры атрибута событий \_ WPD**    | **VT \_ Unknown** | Объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий параметры события.                               |
| **\_ \_ параметры атрибута события \_ WPD** | **VT \_ Unknown** | Объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий параметры события.              |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты**](properties-and-attributes.md)
</dt> </dl>

 

 





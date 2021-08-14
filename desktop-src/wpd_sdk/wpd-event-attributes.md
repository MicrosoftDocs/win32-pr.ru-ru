---
description: 'для Windows 7 Windows портативные устройства поддерживают следующие атрибуты для событий службы устройства. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетевентаттрибутес.'
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
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193295"
---
# <a name="event-attributes-portabledeviceh"></a>Атрибуты событий (Портабледевице. h)

для Windows 7 Windows портативные устройства поддерживают следующие атрибуты для событий службы устройства. Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетевентаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| attribute                             | VarType         | Описание                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ имя атрибута события \_ WPD**       | **VT \_ LPWSTR**  | Строка, указывающая понятное для сценария имя события. Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ". |
| **\_ \_ параметры атрибута событий \_ WPD**    | **VT \_ Unknown** | Объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий параметры события.                               |
| **\_ \_ параметры атрибута события \_ WPD** | **VT \_ Unknown** | Объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий параметры события.              |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты**](properties-and-attributes.md)
</dt> </dl>

 

 





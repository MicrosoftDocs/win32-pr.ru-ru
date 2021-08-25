---
description: Windows Портативные устройства поддерживают следующие свойства атрибутов ресурсов.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Свойства атрибута ресурса (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928074"
---
# <a name="resource-attribute-properties"></a>Свойства атрибута ресурса

Windows Портативные устройства поддерживают следующие свойства атрибутов ресурсов.



| Свойство                                    | VarType         | Описание                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD** | **VT \_ Unknown** | Это [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий одно значение, которое является ключом, идентифицирующим ресурс.                     |
| **\_ \_ Формат атрибута ресурса \_ WPD**        | **VT \_ CLSID**   | Значение идентификатора GUID, указывающее формат ресурса. список форматов, определенных Windows портативных устройств, см. в разделе [форматы объектов](object-format-guids.md) . |
| **\_ \_ \_ Общий \_ Размер атрибута ресурса WPD**   | **VT \_ UI8**     | Общий размер данных ресурса в байтах.                                                                                                                            |



 

## <a name="remarks"></a>Remarks

Эти атрибуты возвращаются методом [**ипортабледевицересаурцес:: жетресаурцеаттрибутес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ипортабледевицересаурцес:: Жетресаурцеаттрибутес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Свойства и атрибуты WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





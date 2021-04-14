---
description: 'Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для форматов в службе устройств. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетформататтрибутес.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Атрибуты формата (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668680"
---
# <a name="format-attributes"></a>Атрибуты формата

Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для форматов в службе устройств. Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетформататтрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .




| **Attribute**                        | **VarType**    | **Описание**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ тип MIME атрибута формата WPD \_** | **VT \_ LPWSTR** | Тип MIME формата.                                                                                                     |
| **\_ \_ имя атрибута формата \_ WPD**     | **VT \_ LPWSTR** | Строка, указывающая понятное для сценария имя формата. Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ". |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты**](properties-and-attributes.md)
</dt> </dl>

 

 





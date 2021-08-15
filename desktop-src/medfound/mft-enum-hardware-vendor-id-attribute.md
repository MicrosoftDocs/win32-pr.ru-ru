---
description: Указывает идентификатор поставщика для Microsoft Media Foundation на основе оборудования.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Атрибут MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff3a93abed968a26f8eead5be6a7d1872b9d4556b0d163632992cbcc21b1acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973103"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>\_ \_ \_ \_ Атрибут атрибута идентификатора поставщика оборудования \_ перечисления MFT

Указывает идентификатор поставщика для преобразования Microsoft Media Foundation на основе оборудования (MFT).

## <a name="data-type"></a>Тип данных

**WCHAR\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarks

Этот атрибут является информационным и необязательным.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>Мфтрансформ. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Оборудование МФТС](hardware-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 





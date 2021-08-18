---
title: Перечисление Сохаттрибутетипе (Наппротокол. h)
description: Задает тип атрибута, хранящегося в объекте-длине типа атрибута (TLV).
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- Сохаттрибутетипе перечисление NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c3fabf3a8911274b912f3762dd07d0c64fc4111d22e372d1962a92221f1d068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939061"
---
# <a name="sohattributetype-enumeration"></a>Перечисление Сохаттрибутетипе

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Перечисление **сохаттрибутетипе** указывает тип атрибута, хранящегося в объекте-длине типа атрибута (TLV).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**сохаттрибутетипесистемхеалсид**
</dt> <dd>

Указывает тип атрибута "идентификатор работоспособности системы".

</dd> <dt>

<span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**
</dt> <dd>

Указывает тип атрибута сервера исправления IPv4.

</dd> <dt>

<span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**сохаттрибутетипекомплианцересулткодес**
</dt> <dd>

Указывает тип атрибута кода результата соответствия.

</dd> <dt>

<span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**сохаттрибутетипетимеофластупдате**
</dt> <dd>

Задает время последнего типа атрибута обновления.

</dd> <dt>

<span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**сохаттрибутетипеклиентид**
</dt> <dd>

Указывает тип атрибута идентификатора клиента.

</dd> <dt>

<span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**сохаттрибутетипевендорспеЦифик**
</dt> <dd>

Указывает тип атрибута, зависящий от поставщика.

</dd> <dt>

<span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**сохаттрибутетипехеалскласс**
</dt> <dd>

Указывает тип атрибута класса работоспособности.

</dd> <dt>

<span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**сохаттрибутетипесофтвареверсион**
</dt> <dd>

Указывает тип атрибута версии программного обеспечения.

</dd> <dt>

<span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**сохаттрибутетипепродуктнаме**
</dt> <dd>

Указывает тип атрибута «Название продукта».

</dd> <dt>

<span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**сохаттрибутетипехеалсклассстатус**
</dt> <dd>

Указывает тип атрибута состояния класса работоспособности.

</dd> <dt>

<span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**сохаттрибутетипесохженератионтиме**
</dt> <dd>

Указывает время формирования инструкции типа атрибута работоспособности.

</dd> <dt>

<span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**сохаттрибутетипирроркодес**
</dt> <dd>

Задает тип атрибута кода ошибки.

</dd> <dt>

<span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**сохаттрибутетипефаилурекатегори**
</dt> <dd>

Указывает тип атрибута категории сбоев.

</dd> <dt>

<span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**
</dt> <dd>

Указывает тип атрибута сервера исправления IPv6.

</dd> <dt>

<span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**сохаттрибутетипикстендедисолатионстате**
</dt> <dd>

Задает расширенный тип атрибута состояния изоляции.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура [**сохаттрибутевалуе**](sohattributevalue-union.md) определяет значения атрибутов, соответствующие каждому типу атрибута.

Эти типы атрибутов используются системой защиты доступа к сети:

-   сохаттрибутетипесистемхеалсид
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   сохаттрибутетипекомплианцересулткодес
-   сохаттрибутетипефаилурекатегори

Остальные типы предназначены только для помощи SHA и SHV.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сохаттрибутевалуе**](sohattributevalue-union.md)
</dt> <dt>

[**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[**Состояния**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[**инапсохконструктор**](inapsohconstructor.md)
</dt> <dt>

[**инапсохпроцессор**](inapsohprocessor.md)
</dt> </dl>

 

 






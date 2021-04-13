---
title: Объединение Сохаттрибутевалуе (Наппротокол. h)
description: Определяет содержимое члена типа в структуре Сохаттрибуте.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- Сохаттрибутевалуе объединения NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492333"
---
# <a name="sohattributevalue-union"></a>Объединение Сохаттрибутевалуе

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Объединение **сохаттрибутевалуе** определяет содержимое члена **типа** в структуре [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) . Структура объединения **сохаттрибутевалуе** определяется [**сохаттрибутетипе**](sohattributetype-enum.md) , указанным в элементе **Type** структуры [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .

## <a name="syntax"></a>Синтаксис


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>Члены

<dl> <dt>

**идвал**
</dt> <dd>

**регистр (Сохаттрибутетипесистемхеалсид)**

Уникальный [системхеалсентитид](nap-datatypes.md) , содержащий идентификатор агента работоспособности системы (SHA) или средство проверки работоспособности системы (SHV), в котором был создан этот пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**регистр (sohAttributeTypeIpv4FixupServers)**

IPv4-адреса серверов исправления, используемых системой защиты доступа к сети.

<dl> <dt>

**count**
</dt> <dd>

Число IPv4-адресов в члене **addresses** в диапазоне от 1 до [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**Addresses**
</dt> <dd>

Массив структур [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) , содержащих IPv4-адреса.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**регистр (sohAttributeTypeIpv6FixupServers)**

IPv6-адреса серверов исправления, используемых системой защиты доступа к сети.

<dl> <dt>

**count**
</dt> <dd>

Число IPv4-адресов в члене **addresses** в диапазоне от 1 до [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**Addresses**
</dt> <dd>

Массив структур [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) , содержащих IPv4-адреса.

</dd> </dl> </dd> <dt>

**кодесвал**
</dt> <dd>

**Case (Сохаттрибутетипекомплианцересулткодес, Сохаттрибутетипирроркодес)**

Структура [**ресулткодес**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) , содержащая либо определенные приложением коды результатов соответствия констант клиента, либо [**ошибки NAP**](nap-error-constants.md). Пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) должен содержать этот TLV или TLV **сохаттрибутетипефаилурекатегори** .

</dd> <dt>

**датетимевал**
</dt> <dd>

**Case (Сохаттрибутетипетимеофластупдате, Сохаттрибутетипесохженератионтиме)**

Структура [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , которая содержит время последнего обновления [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) или время создания **состояния работоспособности** .

</dd> <dt>

**вендорспеЦификвал**
</dt> <dd>

**регистр (СохаттрибутетипевендорспеЦифик)**

Зависящие от приложения данные, определяемые поставщиком.

<dl> <dt>

**Поставщика**
</dt> <dd>

4-байтовый идентификатор, который определяет идентификатор пары SHA/SHV. Первые 3 байта — это код SMI поставщика, назначенный IETF, а последний байт идентифицирует сам компонент. При реализации SHA или SHV не используйте значения ИДЕНТИФИКАТОРов, назначенные внутренним компонентам работоспособности системы Майкрософт на [**константах поставщика NAP**](nap-vendor-constants.md).

</dd> <dt>

**size**
</dt> <dd>

Размер (в байтах) данных поставщика в диапазоне от 0 до ([**макссохаттрибутесизе**](nap-type-constants.md) -4).

</dd> <dt>

**вендорспеЦификдата**
</dt> <dd>

Указатель на данные конкретного поставщика в сетевом порядке байтов.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**Case (Сохаттрибутетипехеалскласс, Сохаттрибутетипефаилурекатегори, Сохаттрибутетипикстендедисолатионстате)**

Класс работоспособности, Категория сбоя или Расширенное состояние изоляции компонента NAP как значение [**хеалсклассвалуе**](healthclassvalue-enum.md) или [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) или структура [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .

</dd> <dt>

**октетстрингвал**
</dt> <dd>

**default**

Следующие значения атрибутов являются строками октета:

-   сохаттрибутетипесофтвареверсион
-   сохаттрибутетипеклиентид
-   сохаттрибутетипепродуктнаме
-   сохаттрибутетипехеалсклассстатус

Для прямой совместимости все нераспознанные атрибуты возвращаются в виде строк октета. **данные** должны быть в сетевом порядке байтов.

<dl> <dt>

**size**
</dt> <dd>

Размер (в байтах) **данных** в диапазоне от 0 до [**макссохаттрибутесизе**](nap-type-constants.md).

</dd> <dt>

**data**
</dt> <dd>

Указатель на значение строки октета.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Структура фактических данных

Из-за природы среды публикации SDK объединения не представляются явно в блоках синтаксиса. Ниже приведен фактический синтаксис из файла заголовка Наппротокол. h.


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>Комментарии

Эти типы атрибутов используются системой защиты доступа к сети:

-   сохаттрибутетипесистемхеалсид
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   сохаттрибутетипекомплианцересулткодес
-   сохаттрибутетипефаилурекатегори

Остальные [**сохаттрибутетипес**](sohattributetype-enum.md) предназначены исключительно в качестве нормативных руководств по использованию SHA и SHV.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по NAP](nap-reference.md)
</dt> <dt>

[Структуры NAP](nap-structures.md)
</dt> </dl>

 


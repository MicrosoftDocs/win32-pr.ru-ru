---
title: Класс Win32_TSLicenseReportPerDeviceEntry
description: Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на устройство (RDS \ 160; CAL на устройство).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportPerDeviceEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportPerDeviceEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008424"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>\_Класс Win32 тслиценсерепортпердевицеентри

Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии для каждого устройства (клиентская лицензия RDS на устройство).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепортпердевицеентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ тслиценсерепортпердевицеентри** имеет следующие свойства.

<dl> <dt>

**калтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип выданной лицензии CAL. Это может быть одно из следующих значений.

"Встроенная клиентская лицензия служб терминалов" на устройство "

"Клиентская лицензия" TS per Device "

"Клиентская лицензия TS подключателя к Интернету"

"TS CAL на пользователя"

"TS или RDS per Device CAL"

Клиентские лицензии TS или RDS на пользователя

Лицензия "Стандартный набор VDI Standard Suite для подписки устройств"

лицензия "VDI Premium Suite" для подписки устройства "

"RDS per Device CAL"

"RDS на пользователя CAL"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата окончания срока действия лицензии.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS на пользователя. Это может быть одно из следующих значений.

<dt>

"Windows Server 2012"
</dt> <dd>

с этой лицензией поддерживаются только серверы Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

с этой лицензией поддерживаются только серверы, работающие под Windows server 2008 R2 или Windows server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

с этой лицензией поддерживаются только серверы, работающие под Windows Server 2008.

</dd> </dl>

</dd> <dt>

**продуктверсионид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор версии продукта для службы удаленных рабочих столов пакета лицензионных ключей.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Не поддерживается.

</dd> <dt>

0
</dt> <dd>

Не поддерживается.

</dd> </dl>

</dd> <dt>

**шардвареид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Идентификатор оборудования компьютера.

</dd> <dt>

**сиссуедтокомпутер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, для которого предпринималась попытка выдачи лицензии.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**фетчрепортпердевицеентриес**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 


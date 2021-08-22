---
title: Класс Win32_TSLicenseReportSummaryEntry
description: Содержит сводку по установленным и выпущенным службы удаленных рабочих столов клиентских лицензий на доступ для пользователей (RDS \ 160; CAL на пользователя).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportSummaryEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportSummaryEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137806"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>\_Класс Win32 тслиценсерепортсуммарентри

Содержит сводку по установленным и выпущенным службы удаленных рабочих столов клиентских лицензий на клиентские лицензии (RDS на пользователя).

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепортсуммарентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ тслиценсерепортсуммарентри** имеет следующие свойства.

<dl> <dt>

**инсталледлиценсес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число установленных клиентских лицензий служб удаленных рабочих столов "на пользователя".

</dd> <dt>

**иссуедлиценсес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число выданных клиентских лицензий RDS "на пользователя".

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия службы удаленных рабочих столов, для которой была выдана клиентская лицензия RDS "на пользователя".

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

**тскалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступность клиентских лицензий RDS "на пользователя". Это может быть одно из следующих значений.

<dt>

Имеющ
</dt> <dd>

Доступны клиентские лицензии RDS "на пользователя".

</dd> <dt>

Ограничены
</dt> <dd>

Доступность клиентских лицензий служб удаленных рабочих столов "на пользователя" ограничена.

</dd> <dt>

"None"
</dt> <dd>

Клиентские лицензии RDS "на пользователя" недоступны.

</dd> <dt>

"Not Tracking"
</dt> <dd>

Доступность клиентских лицензий служб удаленных рабочих столов "на пользователя" не отслеживается.

</dd> </dl>

</dd> <dt>

**тскалтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип клиентских лицензий служб удаленных рабочих столов "на пользователя". Это может быть одно из следующих значений.

<dt>

"На устройство"
</dt> <dd>

Для каждого устройства выдаются клиентские лицензии RDS "на пользователя".

</dd> <dt>

"На пользователя"
</dt> <dd>

Клиентские лицензии RDS "на пользователя" выдаются для каждого пользователя.

</dd> <dt>

Неизвестный
</dt> <dd>

Тип клиентских лицензий служб удаленных рабочих столов "на пользователя" неизвестен.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 






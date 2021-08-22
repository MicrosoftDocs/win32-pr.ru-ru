---
title: Класс Win32_TSLicenseReportFailedPerUserEntry
description: Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на пользователя (RDS \ 160; CAL на пользователя).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportFailedPerUserEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportFailedPerUserEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02d56c1a7e2c715f068d808d45ac6ae3295b16bb7382179ec0e32c93beee096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420844"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>\_Класс Win32 тслиценсерепортфаиледперусерентри

Содержит сведения о неудачном службы удаленных рабочих столов клиентской лицензии на пользователя (RDS на пользователя CAL).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепортфаиледперусерентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ тслиценсерепортфаиледперусерентри** имеет следующие свойства.

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

**триедиссуанцеон**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата попыток выдачи лицензии.

</dd> <dt>

**Пользователь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя пользователя, которому предпринималась попытка выдачи лицензии.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фетчрепортфаиледперусерентриес**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 


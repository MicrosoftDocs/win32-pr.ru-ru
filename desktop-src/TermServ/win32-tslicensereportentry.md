---
title: Класс Win32_TSLicenseReportEntry
description: Содержит сведения о выданной службы удаленных рабочих столов клиентской лицензии для каждого пользователя (RDS \ 160; CAL на пользователя).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414828"
---
# <a name="win32_tslicensereportentry-class"></a>\_Класс Win32 тслиценсерепортентри

Содержит сведения о выданной службы удаленных рабочих столов клиентской лицензии для каждого пользователя (клиентские лицензии служб удаленных рабочих столов на пользователя).

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепортентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тслиценсерепортентри** имеет следующие свойства.

<dl> <dt>

**калтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип выданной лицензии CAL. Это может быть одно из следующих значений.

**Windows server 2008 R2 и Windows server 2008:** Это свойство не поддерживается.

"Встроенная клиентская лицензия служб терминалов" на устройство "

"Клиентская лицензия" TS per Device "

"Клиентская лицензия TS подключателя к Интернету"

"TS CAL на пользователя"

"TS или RDS per Device CAL"

Клиентские лицензии TS или RDS на пользователя

Лицензия "Стандартный набор VDI Standard Suite для подписки устройств"

Лицензия "VDI Premium Suite с подпиской на устройство"

"RDS per Device CAL"

"RDS на пользователя CAL"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата окончания срока действия лицензии, выданной пользователю.

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

С этой лицензией поддерживаются только серверы под Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008.

</dd> <dt>

Windows Server 7
</dt> <dd>

С этой лицензией поддерживаются только серверы, работающие под Windows Server 2008 R2 или Windows Server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

С этой лицензией поддерживаются только серверы под под Windows Server 2008.

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

**Пользователь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя пользователя, которому была выдана лицензия.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для использования этого класса необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фетчрепортентриес**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**\_Тсиссуедлиценсе Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_Тслиценсерепорт Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 


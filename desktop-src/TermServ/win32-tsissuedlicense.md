---
title: Класс Win32_TSIssuedLicense
description: Описывает экземпляры клиентских лицензий службы удаленных рабочих столов для каждого устройства (RDS \ 160; CAL "на устройство"), выпущенных на сервере лицензий удаленный рабочий стол.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSIssuedLicense службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSIssuedLicense, описание
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76127d41c6a571b6bc75bc74378b21f76f4b38c05f0a223d36e979dccf89a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656164"
---
# <a name="win32_tsissuedlicense-class"></a>\_Класс Win32 тсиссуедлиценсе

Описывает экземпляры лицензий на клиентский доступ службы удаленных рабочих столов на устройство (клиентские лицензии на устройства), выданные с сервера лицензий удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсиссуедлиценсе** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсиссуедлиценсе** содержит следующие методы.



| Метод                                         | Описание                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**REVOKE**](revoke-win32-tsissuedlicense.md) | Отменяет клиентские лицензии RDS "на устройство", представленные объектом **Win32 \_ тсиссуедлиценсе** .<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсиссуедлиценсе** имеет следующие свойства.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает дату истечения срока действия лицензии.

</dd> <dt>

**иссуедате**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает дату выдачи лицензии.

</dd> <dt>

**кэйпаккид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Идентифицирует службы удаленных рабочих столов пакет лицензионных ключей.

</dd> <dt>

**лиценсеид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальный идентификатор для этой лицензии.

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние лицензии.

<dt>

0
</dt> <dd>

Состояние лицензии неизвестно.

</dd> <dt>

1
</dt> <dd>

Лицензия является временной лицензией.

</dd> <dt>

2
</dt> <dd>

Лицензия активна.

</dd> <dt>

3
</dt> <dd>

Лицензия является лицензией на обновление.

</dd> <dt>

4
</dt> <dd>

Лицензия была отозвана.

</dd> <dt>

5
</dt> <dd>

Состояние лицензии — ожидание.

</dd> <dt>

6
</dt> <dd>

Лицензия является параллельной лицензией.

</dd> </dl>

</dd> <dt>

**шардвареид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор оборудования, для которого была выдана лицензия.

</dd> <dt>

**сиссуедтокомпутер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, для которого была выдана лицензия.

</dd> <dt>

**сиссуедтаусер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя пользователя, для которого была выдана лицензия.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для использования этого класса необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_Тслиценсерепорт Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_Тслиценсерепортентри Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 


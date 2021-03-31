---
title: Класс Win32_TSLicenseReportFailedPerUserSummaryEntry
description: Содержит сведения о доменах, для которых не удалось выдачу на пользователя.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReportFailedPerUserSummaryEntry службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReportFailedPerUserSummaryEntry, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988254"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a>\_Класс Win32 тслиценсерепортфаиледперусерсуммарентри

Содержит сведения о доменах, для которых не удалось выдачу на пользователя.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепортфаиледперусерсуммарентри** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тслиценсерепортфаиледперусерсуммарентри** имеет следующие свойства.

<dl> <dt>

**Имя_домена**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Указывает имя домена, в котором произошел сбой при выдаче лицензии.

</dd> <dt>

**фаиледиссуанцекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество неудачных выдачи.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Тлсвмипров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фетчрепортфаиледперусерсуммарентриес**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 


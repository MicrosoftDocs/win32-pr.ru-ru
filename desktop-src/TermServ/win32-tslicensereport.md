---
title: Класс Win32_TSLicenseReport
description: Предоставляет экземпляры клиентской лицензии службы удаленных рабочих столов на пользователя (RDS \ 160; Отчеты об использовании CAL "на пользователя", созданные на сервере лицензий удаленный рабочий стол, а также методы создания, выборки и удаления отчетов по лицензиям.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseReport службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseReport, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93280c00cbd20993907901e1f9b8c16330863a47bddd4e08bc86d51b4b837233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137837"
---
# <a name="win32_tslicensereport-class"></a>\_Класс Win32 тслиценсерепорт

Содержит экземпляры службы удаленных рабочих столов клиентских лицензий (RDS на пользователя), созданных на сервере лицензирования удаленный рабочий стол, а также методы создания, получения и удаления отчетов по лицензиям.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тслиценсерепорт** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тслиценсерепорт** содержит следующие методы.



| Метод                                                                                                         | Описание                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Удаляет объект отчета на сервере лицензирования удаленный рабочий стол. Это не статический метод.<br/>                                                                                           |
| [**фетчрепортентриес**](fetchreportentries-win32-tslicensereport.md)                                         | Извлекает записи в объекте отчета.<br/>                                                                                                                                              |
| [**фетчрепортфаиледперусерентриес**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Получает сведения о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.<br/>                                                             |
| [**фетчрепортфаиледперусерсуммарентриес**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Получение сводных данных о неудачных службы удаленных рабочих столов клиентских лицензиях на клиентские лицензии (RDS на пользователя) из отчета.<br/>                                                 |
| [**фетчрепортпердевицеентриес**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Получение сведений о выданных лицензиях на клиентский доступ службы удаленных рабочих столов для каждого устройства (клиентские лицензии служб удаленных рабочих столов на устройство) из отчета.<br/>                                                     |
| [**фетчрепортсуммарентриес**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Извлекает сводки лицензий из объекта отчета.<br/>                                                                                                                                  |
| [**Создание отчета.**](generatereport-win32-tslicensereport.md)                                                 | Этот метод не поддерживается.<br/> **Windows server 2008 R2 и Windows server 2008:** Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.<br/> |
| [**женератерепортекс**](generatereportex-win32-tslicensereport.md)                                             | Формирует текущий отчет об использовании лицензий на пользователя на сервере лицензирования удаленный рабочий стол.<br/>                                                                                              |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тслиценсерепорт** имеет следующие свойства.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя отчета.

</dd> <dt>

**женератиондатетиме**
</dt> <dd> <dl> <dt>

Тип данных: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания отчета лицензирования удаленных рабочих столов.

</dd> <dt>

**инсталледлиценсес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Данное свойство не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Число установленных клиентских лицензий служб удаленных рабочих столов "на пользователя".

</dd> <dt>

**лиценсеусажекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Данное свойство не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Количество клиентских лицензий служб удаленных рабочих столов "на пользователя", которые в настоящее время используются.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Данное свойство не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Тип области отчета лицензирования удаленных рабочих столов.

</dd> <dt>

**скопевалуе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Данное свойство не поддерживается.

**Windows server 2008 R2 и Windows server 2008:** Значение области отчета лицензирования удаленных рабочих столов.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия отчета лицензирования удаленных рабочих столов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Отчеты, созданные с помощью WMI, отображаются в диспетчере лицензирования удаленных рабочих столов. Отчеты, удаленные с помощью WMI, также удаляются из диспетчера лицензирования удаленных рабочих столов.

Для использования этого класса необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тсиссуедлиценсе Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_Тслиценсекэйпакк Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_Тслиценсерепортентри Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_Тслиценсесервер Win32**](win32-tslicenseserver.md)
</dt> </dl>

 


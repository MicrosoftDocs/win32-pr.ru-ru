---
title: Класс Win32_TSCPubPlugin
description: Представляет подключаемый модуль, настроенный для использования в службе управление подключениями к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSCPubPlugin службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSCPubPlugin, описание
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891817"
---
# <a name="win32_tscpubplugin-class"></a>\_Класс Win32 тскпубплугин

Представляет подключаемый модуль, настроенный для использования в службе управление подключениями к удаленным рабочим столам и приложениям RemoteApp.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тскпубплугин** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тскпубплугин** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое описание (однострочная строка) объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ЭТОМУ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Идентификатор CLSID подключаемого модуля.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF
</dt> </dl>

Дата установки объекта. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**IsEnabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включен ли подключаемый модуль.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

<dt>



 ("ОК")


</dt> <dd></dd> <dt>



 ("Ошибка")


</dt> <dd></dd> <dt>



 ("Пониженное состояние")


</dt> <dd></dd> <dt>



 ("Неизвестно")


</dt> <dd></dd> <dt>



 ("Пред Fail")


</dt> <dd></dd> <dt>



 ("Запуск")


</dt> <dd></dd> <dt>



 ("Остановка")


</dt> <dd></dd> <dt>



 ("Служба")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Тскпуб. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 


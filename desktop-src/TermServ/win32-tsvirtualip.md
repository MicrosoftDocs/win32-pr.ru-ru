---
title: Класс Win32_TSVirtualIP
description: Определяет параметры виртуализации IP для сервера узла сеансов удаленный рабочий стол.
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVirtualIP службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVirtualIP, описание
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28830e44fd54e9246cb0affc5fdde1427673d92e843adfd3e1e19cd221af370e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769054"
---
# <a name="win32_tsvirtualip-class"></a>\_Класс Win32 тсвиртуалип

Определяет параметры виртуализации IP для сервера узла сеансов удаленный рабочий стол.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсвиртуалип** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсвиртуалип** содержит следующие методы.



| Метод                                                                                                   | Описание                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддпрограм**](addprogram-win32-tsvirtualip.md)                                                       | Добавляет программу в список программ, использующих виртуализацию IP-адресов.<br/>                                                                                                |
| [**ремовепрограм**](removeprogram-win32-tsvirtualip.md)                                                 | Удаляет программу из списка программ, использующих виртуализацию IP-адресов.<br/>                                                                                           |
| [**селектнетворкадаптер**](selectnetworkadapter-win32-tsvirtualip.md)                                   | Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.<br/>                                                                                         |
| [**сетпрограмлист**](setprogramlist-win32-tsvirtualip.md)                                               | Перезаписывает список программ, использующих виртуализацию IP.<br/>                                                                                                       |
| [**сетвиртуалипактиве**](setvirtualipactive-win32-tsvirtualip.md)                                       | Задает значение свойства **виртуалипактиве** .<br/>                                                                                                                      |
| [**сетвиртуалипмоде**](setvirtualipmode-win32-tsvirtualip.md)                                           | Задает значение свойства **виртуалипмоде** .<br/>                                                                                                                        |
| [**сетвиртуализелупбаккаддрессесенаблед**](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | Задает значение свойства **виртуализелупбаккаддрессесенаблед** .<br/> **Windows Server 2008 R2:** Этот метод недоступен до Windows Server 2012.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсвиртуалип** имеет следующие свойства.

<dl> <dt>

**Caption**
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

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**нетворкадаптердескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание сетевого адаптера.

</dd> <dt>

**нетворкадаптердескриптионлист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список описаний доступных физических сетевых адаптеров.

</dd> <dt>

**нетворкадаптермакаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

MAC-адрес сетевого адаптера.

</dd> <dt>

**нетворкадаптермаклист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список MAC-адресов доступных физических сетевых адаптеров.

</dd> <dt>

**полицисаурценетворкадаптер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроен ли сетевой адаптер сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцепрограмлист**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **програмлист** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцевиртуалипактиве**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **виртуалипактиве** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцевиртуалипмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **виртуалипмоде** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**програмлист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает программы, настроенные для использования виртуализации IP. Это может быть имя программы или полный путь.

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

</dd> <dt>

**виртуалипактиве**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Указывает, активна ли на сервере виртуализация IP-адресов. Это может быть одно из следующих значений.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Виртуализация IP-адресов неактивна.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Виртуализация IP-адресов активна.

</dd> </dl>

</dd> <dt>

**виртуалипмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, какой режим виртуализации IP используется на сервере. Это может быть одно из следующих значений.

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**За сеанс** (0)


</dt> <dd>

Режим виртуализации IP — для каждого сеанса.

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**На программу** (1)


</dt> <dd>

Режим виртуализации IP-адресов — "на пользователя".

</dd> </dl>

</dd> <dt>

**виртуализелупбаккаддрессесенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включена ли виртуализация адресов замыкания на себя.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Не включено

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Активировано

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 


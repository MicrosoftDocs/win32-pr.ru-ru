---
title: Класс Win32_TSRemoteControlSetting
description: Определяет параметры конфигурации удаленного управления для \_ класса терминала Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSRemoteControlSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSRemoteControlSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490965"
---
# <a name="win32_tsremotecontrolsetting-class"></a>\_Класс Win32 тсремотеконтролсеттинг

Класс **WMI \_ тсремотеконтролсеттинг** инструментария Win32 определяет параметры конфигурации удаленного управления для класса [**\_ терминала Win32**](win32-terminal.md) .

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсремотеконтролсеттинг** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсремотеконтролсеттинг** содержит следующие методы.



| Метод                                                              | Описание                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [**ремотеконтрол**](win32-tsremotecontrolsetting-remotecontrol.md) | Задает свойство **левелофконтрол** этого класса.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсремотеконтролсеттинг** имеет следующие свойства.

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

**левелофконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уровень контроля для сеанса, который указывает, будет ли сеанс просматриваться только удаленным пользователем или просматриваться и контролироваться с помощью клавиатуры и мыши. Дополнительные сведения см. в подразделе "Примечания" метода [**ремотеконтрол**](win32-tsremotecontrolsetting-remotecontrol.md) . Поддерживаются следующие значения.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (0)


</dt> <dd>

Удаленное управление отключено.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**Енаблеинпутнотифи** (1)


</dt> <dd>

Пользователь удаленного управления имеет полный контроль над сеансом пользователя с разрешением пользователя.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**Енаблеинпутнонотифи** (2)


</dt> <dd>

Пользователь удаленного управления имеет полный контроль над сеансом пользователя; разрешение пользователя не требуется.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**Енабленоинпутнотифи** (3)


</dt> <dd>

Пользователь удаленного управления может просматривать сеанс удаленно с разрешением пользователя; удаленный пользователь не может активно управлять сеансом.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**Енабленоинпутнонотифи** (4)


</dt> <dd>

Пользователь удаленного управления может просматривать сеанс удаленно, но не управляет им активно. разрешение пользователя не требуется.

</dd> </dl>

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

**полицисаурцелевелофконтрол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **левелофконтрол** сервером, групповой политикой или по умолчанию.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> <dt>

2 (0x2)
</dt> <dd>

Значение по умолчанию

</dd> </dl>

</dd> <dt>

**ремотеконтролполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Политика, используемая сервером для получения параметров удаленного управления.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)


</dt> <dd>

Параметры удаленного управления пользователя вступают в действие.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)


</dt> <dd>

Параметры удаленного управления пользователя переопределяются сервером.

</dd> </dl>

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

**терминалнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя терминала.

Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". Для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6. В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминал Win32**](win32-terminal.md)
</dt> <dt>

[**\_Терминалсеттинг Win32**](win32-terminalsetting.md)
</dt> </dl>

 


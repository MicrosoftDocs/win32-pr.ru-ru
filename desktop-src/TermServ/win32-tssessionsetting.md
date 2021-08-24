---
title: Класс Win32_TSSessionSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, такие как ограничения времени, а также действия по отсоединению и повторному подключению.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSessionSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSessionSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5139b53917f3d54b95fd153ac39fab176f047ba4bb9ec6df5d1c7c9b6e2d2f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769154"
---
# <a name="win32_tssessionsetting-class"></a>\_Класс Win32 тссессионсеттинг

Класс **WMI \_ тссессионсеттинг** инструментария Win32 определяет параметры конфигурации для [**класса \_ терминала Win32**](win32-terminal.md) , например ограничения по времени, а также действия по отсоединению и повторному подключению.

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тссессионсеттинг** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тссессионсеттинг** содержит следующие методы.



| Метод                                                              | Описание                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**брокенконнектион**](win32-tssessionsetting-brokenconnection.md) | Задает свойства разорванного соединения, входящие в этот класс.<br/> |
| [**тимелимит**](win32-tssessionsetting-timelimit.md)               | Задает свойства предела времени, включаемые в этот класс.<br/>        |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тссессионсеттинг** имеет следующие свойства.

<dl> <dt>

**активесессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество времени в миллисекундах, выделенное для активного сеанса. Значение 0 указывает на бесконечное количество времени.

</dd> <dt>

**брокенконнектионактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, которое сервер принимает в сеансе, когда подключение разорвано из-за потери сети или превышения предельного времени.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Отключить** (0)


</dt> <dd>

Пользователь отключен от сеанса.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (1)


</dt> <dd>

Сеанс окончательно удаляется с сервера.

</dd> </dl>

</dd> <dt>

**брокенконнектионполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Политика, используемая сервером для определения времени разрыва подключения из-за потери сети или превышения предельного времени.

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)


</dt> <dd>

Параметры политики отключения пользователя переопределяются сервером.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)


</dt> <dd>

Параметры политики отключения пользователя вступают в действие.

</dd> </dl>

</dd> <dt>

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

**дисконнектедсессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени (в миллисекундах), по истечении которого отключенный сеанс завершается. Значение 0 указывает на бесконечное количество времени.

</dd> <dt>

**енаблетимеаутварнинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Включает предупреждение о превышении времени ожидания.

**Windows 7, Windows server 2008 R2, Windows Vista и Windows Server 2008:** Это свойство недоступно.

</dd> <dt>

**идлесессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени в миллисекундах, по истечении которого бездействующий сеанс завершается. Значение 0 указывает на бесконечное количество времени.

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

**полицисаурцеактивесессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **активесессионлимит** сервером, групповой политикой или по умолчанию.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> <dt>

2
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцеброкенконнектионактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **брокенконнектионактион** сервером, групповой политикой или по умолчанию.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> <dt>

2
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцедисконнектедсессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **дисконнектедсессионлимит** сервером, групповой политикой или по умолчанию.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> <dt>

2
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцеидлесессионлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **идлесессионлимит** сервером, групповой политикой или по умолчанию.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> <dt>

2
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**полицисаурцереконнектионполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **реконнектполици** сервером, групповой политикой или по умолчанию.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика

</dd> <dt>

2
</dt> <dd>

По умолчанию

</dd> </dl>

</dd> <dt>

**реконнектионполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, должен ли пользователь использовать предыдущий клиент для повторного подключения к отключенному сеансу.

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Любой клиент** (0)


</dt> <dd>

Любой клиент будет использоваться для повторного подключения.

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Предыдущий клиент** (1)


</dt> <dd>

Предыдущий клиент, используемый в соединении, будет использоваться для повторного подключения.

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

</dd> <dt>

**тимелимитполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Политика, используемая сервером для определения ограничений по времени для пользовательских сеансов.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)


</dt> <dd>

Действуют параметры политики ограничения времени пользователя.

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Переопределение сервера** (1)


</dt> <dd>

Параметры политики ограничения времени пользователя переопределяются сервером.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Имейте в виду, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса. Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства Терминалнаме, методы этого объекта будут возвращать **WBEM \_ E \_ не \_ поддерживаются**. Этот код ошибки также будет возвращен, если станция Windows пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.

Чтобы подключиться к \\ \\ пространству имен root cimv2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6. в следующем примере Visual Basic scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Терминалсеттинг Win32**](win32-terminalsetting.md)
</dt> <dt>

[**\_Параметр CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 


---
title: Класс Win32_Terminal
description: Представляет терминал.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Класс Win32_Terminal службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_Terminal, описание
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135382"
---
# <a name="win32_terminal-class"></a>\_Класс терминала Win32

Класс **WMI \_ терминала Win32** представляет терминал.

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a>Члены

Класс **\_ терминала Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ терминала Win32** содержит следующие методы.



| Метод                                  | Описание                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Создания**](create-win32-terminal.md) | Создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов классов [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) .<br/> |
| [**Удалить**](delete-win32-terminal.md) | Удаляет указанный терминал.<br/>                                                                                                                                              |
| [**Включить**](win32-terminal-enable.md) | Отключает или включает терминал.<br/>                                                                                                                                            |
| [**Имени**](win32-terminal-rename.md) | Переименовывает терминал.<br/>                                                                                                                                                        |



 

### <a name="properties"></a>Свойства

Класс **\_ терминала Win32** имеет следующие свойства.

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

**фенаблетерминал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, отключен ли или включен указанный терминал.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Терминал отключен.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Терминал включен.

</dd> </dl>

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

**логжедонусерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число сеансов, вошедших в систему терминала.

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

</dd> <dt>

**терминалнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальное имя, идентифицирующее экземпляр терминала.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Win32 \_ Терминал** связан с [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) в качестве свойства **element** ассоциации [**Win32 \_ терминалтерминалсеттинг**](win32-terminalterminalsetting.md) .

Следующие классы являются подклассами класса **\_ терминала Win32** : [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md), [**Win32 \_ тслогонсеттинг**](win32-tslogonsetting.md), [**Win32 \_ тссессионсеттинг**](win32-tssessionsetting.md), [**Win32 \_ тсенвиронментсеттинг**](win32-tsenvironmentsetting.md), [**Win32 \_ тсремотеконтролсеттинг**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)и [**Win32 \_ TSAccount**](win32-tsaccount.md).

Обратите внимание, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса. Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства **терминалнаме** , методы этого объекта возвращают **WBEM \_ E \_ не \_ поддерживаются**. Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.

Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6. В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


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

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> <dt>

[**\_Терминалтерминалсеттинг Win32**](win32-terminalterminalsetting.md)
</dt> </dl>

 


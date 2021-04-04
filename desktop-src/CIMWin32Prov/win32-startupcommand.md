---
description: '&Win32 \_ стартупкомманд \# 8194; Класс WMI представляет команду, которая запускается автоматически при входе пользователя в систему компьютера.'
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Класс Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896349"
---
# <a name="win32_startupcommand-class"></a>\_Класс Win32 стартупкомманд

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ стартупкомманд для Win32** представляет команду, которая выполняется автоматически при входе пользователя в систему компьютера.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ стартупкомманд** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ стартупкомманд** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**Команда**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) («Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run»)
</dt> </dl>

Команда, выполняемая командой Startup.

Инструментарий WMI получает эти данные из раздела реестра

**HKey \_ По на локальном \_ компьютере** \\  \\  \\ Запуск Microsoft **Windows** \\ **CurrentVersion** \\ 

Пример: "C: \\ Windows \\notepad.exe myfile.txt"

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**Расположение**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")
</dt> </dl>

Путь, по которому команда запуска находится на дисковой файловой системе.

Например: HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Общий запуск** (обычный запуск)


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\ Программное обеспечение \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** («HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run»)


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\ Программное обеспечение \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ рунсервицес** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ рунсервицес")


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| кфиленаме")
</dt> </dl>

Имя файла команды запуска.

Пример: "Финдфаст"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**Пользователь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Имя пользователя, для которого будет запускаться эта команда запуска.

Пример: "mydomain \\ myname"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Свойство «код свойства» указывает идентификатор безопасности пользователя, для которого будет запускаться эта команда запуска. Это свойство пользователя может быть пустым, но если имя пользователя не удается разрешить (например, в случае удаленного пользователя), оно по-прежнему имеет значение. Свойство полезно для различения команд, связанных с двумя разными пользователями с неразрешенными именами. Может иметь значение NULL, если команда связана с элементами, которые не идентифицируют пользователя, как, например, для всех пользователей.

Пример: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ стартупкомманд** является производным от [**\_ параметра CIM**](cim-setting.md).

Запуск компьютера не заканчивается после загрузки операционной системы. Вместо этого можно настроить операционную систему Windows таким образом, чтобы команды запуска запускались при каждом запуске Windows. Команды запуска хранятся в реестре или в составе профиля пользователя и используются для автоматического запуска определенных сценариев или приложений при каждой загрузке Windows.

В большинстве случаев программы автозапуска полезны. они гарантируют, что определенные приложения, такие как антивирусные программы, автоматически запускаются и запускаются при каждой загрузке Windows. Однако программы автозапуска также могут отвечать за такие проблемы, как:

-   Компьютеры, которые занимают много времени на запуск. Это может быть результатом большого количества приложений, которые должны запускаться при каждом запуске Windows.
-   Приложения, представленные на панели задач или в диспетчере задач, даже если пользователь не запустил их. Хотя эти приложения не обязательно вызывают проблемы, они могут привести к вызовам службы поддержки от пользователей, которые путают с тем, откуда поступают эти программы и почему они работают.
-   Компьютеры, на которых возникают проблемы, даже если они находятся в состоянии простоя. Эти проблемы часто отслеживаются с командами запуска, которые выполняются, когда никто не знает, что они работают.

Определение приложений и сценариев, автоматически запускаемых при запуске, является важной, но сложной задачей администрирования, так как команды запуска могут храниться во многих разных местах:

-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   Раздел HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKCU \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   systemdrive \\ Documents and Settings \\ All Users \\ Start Program Menus \\ \\ Startup
-   \\загрузить документы и параметры \\ имя пользователя в \\ меню "Пуск" запуск \\ программ \\

Класс WMI Win32 стартупкомманд можно использовать \_ для перечисления программ автозапуска независимо от того, где хранится информация.

Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр. Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию. Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).

Вы можете изменить значения реестра, в которых **Win32 \_ стартупкомманд** получает данные, вызывая методы [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI в скрипте или в C++. Дополнительные сведения см. [в разделе изменение системного реестра](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Примеры

Следующая команда VBScript перечисляет команды запуска на компьютере.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 

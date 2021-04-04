---
description: Представляет среду или системный параметр среды в системе Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Класс Win32_Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896482"
---
# <a name="win32_environment-class"></a>\_Класс среды Win32

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ среды Win32** представляет среду или системный параметр среды в системе Windows. Запрос к этому классу Возвращает переменные среды, найденные в:

**HKey \_ \_** \\  \\  \\ **Управление** \\  \\ **средой** сессионманажер в системе локального компьютера CurrentControlSet

и

**HKey \_** \\ **< Пользовательская >** \\ **Среда**

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a>Члены

Класс **\_ среды Win32** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ среды Win32** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")
</dt> </dl>

Символьная строка, указывающая имя переменной среды на основе Windows. Указав имя переменной, которая еще не существует, приложение создает новую переменную среды.

Пример: "Path"

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Строка, указывающая текущее состояние объекта. Можно определить операционное и нерабочее состояние. Оперативное состояние может включать "ОК", "деградация" и "пред Fail". "Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).

Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание". "Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**системвариабле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Configuration Manager \\ \\ Environment")
</dt> </dl>

Указывает, является ли переменная системной переменной. Системная переменная задается операционной системой и не зависит от параметров среды пользователя.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| система \\ \\ CurrentControlSet \\ \\ управляющего \\ \\ сеанса диспетчером сеансов \\ \\ ")
</dt> </dl>

Имя владельца параметра среды. Он имеет значение <SYSTEM> для параметров, характерных для системы Windows (в отличие от конкретного пользователя) и <DEFAULT> параметров пользователя по умолчанию.

Пример: "JSmith"

</dd> <dt>

**вариаблевалуе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Configuration Manager \\ \\ Environment")
</dt> </dl>

Заполнитель переменной среды на основе Windows. Такие сведения, как каталог файловой системы, могут изменяться с компьютера на компьютер. Операционная система заменяет заполнители для них.

Пример: "% SystemRoot%"

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ среды Win32** является производным от [**CIM \_ системресаурце**](cim-systemresource.md). Этот класс можно использовать для поиска путей к специальным папкам, таким как системная папка или программные файлы на удаленном компьютере. Вот некоторые примеры: WINDIR, системный_корневой_каталог, ProgramFiles и UserProfile. **Win32 \_ Среда** по сути возвращает сведения о том, что можно найти в:

**HKey \_ \_** \\  \\  \\ **Управление** \\  \\ **средой** сессионманажер в системе локального компьютера CurrentControlSet

и

**HKey \_** \\ **< Пользовательская >** \\ **Среда**

Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр. Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию. Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Примеры

В примере [переменных среды на компьютере на основе](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl для получения сведений обо всех переменных среды на компьютере используется инструментарий WMI.

В следующем примере кода VBScript перечисляются переменные среды на локальном компьютере.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



Следующий пример кода на языке VBScript изменяет переменную среды с именем BUILD \_ на значение, введенное пользователем. В скрипте предполагается, что \_ переменная типа сборки уже существует. Если он не существует, сценарий завершается. Входное значение проверяется: оно должно быть "Build1", "Build2" или "Build3", а другое значение не принимается. Функция VBScript [Укасе](https://msdn.microsoft.com/library/aa902519.aspx) делает нечувствительным к входу регистр. Если значение, введенное в, не является одним из трех допустимых значений, сценарий завершается.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
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

[**\_СИСТЕМРЕСАУРЦЕ CIM**](cim-systemresource.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


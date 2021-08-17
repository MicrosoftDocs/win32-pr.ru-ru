---
description: '&Win32 \_ UserAccount \# 32; Класс WMI содержит сведения об учетной записи пользователя в компьютерной системе, на которой работает Windows.'
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Класс Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df907b1686677db8ea895d8788055567e24dc7be7ffe758bcfa82801591a0dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922754"
---
# <a name="win32_useraccount-class"></a>\_Класс Win32 UserAccount

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ UserAccount для Win32** содержит сведения об учетной записи пользователя в компьютерной системе, на которой работает Windows.

> [!Note]  
> Так как **имя** и **домен** являются ключевыми свойствами, перечисление **Win32 \_ UserAccount** в большой сети может негативно сказаться на производительности. Вызов **GetObject** или выполнение запросов к конкретному экземпляру оказывает меньшее влияние.

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ UserAccount** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ UserAccount** содержит следующие методы.



| Метод                                                     | Описание                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**Имени**](rename-method-in-class-win32-useraccount.md) | Позволяет переименование учетной записи пользователя.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ UserAccount** имеет следующие свойства.

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags")
</dt> </dl>

флаги, описывающие характеристики учетной записи пользователя Windows.

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Временная повторяющаяся учетная запись** (256)


</dt> <dd>

**УФ \_ временная \_ \_ учетная запись повторения**

Локальная учетная запись пользователя для пользователей, имеющих основную учетную запись в другом домене. Эта учетная запись предоставляет пользователю доступ только к этому домену — не к домену, который доверяет данному домену.

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Обычная учетная запись** (512)


</dt> <dd>

**\_Обычная \_ учетная запись УФ**

Тип учетной записи по умолчанию, представляющий обычного пользователя.

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Учетная запись междоменного доверия** (2048)


</dt> <dd>

**\_ \_ учетная запись междоменного доверия УФ \_**

Учетная запись для системного домена, который доверяет другим доменам.

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Учетная запись доверия рабочей станции** (4096)


</dt> <dd>

**\_ \_ учетная запись доверия рабочей станции УФ \_**

учетная запись компьютера для компьютерной системы, на которой работает Windows, являющийся членом этого домена.

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Учетная запись доверия сервера** (8192)


</dt> <dd>

**\_ \_ \_ учетная запись доверия сервера УФ**

Учетная запись для системного контроллера домена резервного копирования, который является членом этого домена.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Домен и имя пользователя учетной записи.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Описание учетной записи.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Отключено**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| user \_ info \| УФ \_ аккаунтдисабле")
</dt> </dl>

Windows учетная запись пользователя отключена.

</dd> <dt>

**Доменная**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("домен"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management functions \| имя_домена")
</dt> </dl>

имя домена Windows, к которому принадлежит учетная запись пользователя, например "нд-SALES".

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетями \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ полное \_ имя**")
</dt> </dl>

Полное имя локального пользователя, например: "Уилсон (".

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Дата установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **fixed**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Если **значение — true**, учетная запись определена на локальном компьютере.

Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).

</dd> <dt>

**Блокирование**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ Блокировка**")
</dt> </dl>

если **значение — true**, учетная запись пользователя заблокирована для операционной системы Windows.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("имя"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| ")
</dt> </dl>

имя учетной записи пользователя Windows в домене, указанном в свойстве **domain** данного класса.

Пример: "данвилсон".

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**пассвордчанжеабле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ PASSWD не \_ удается \_ изменить**")
</dt> </dl>

Если **значение — true**, пароль этой учетной записи пользователя можно изменить.

</dd> <dt>

**пассвордекспирес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**user \_ info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ не \_ Expires WITH \_ PASSWD**")
</dt> </dl>

Если задано **значение true**, то срок действия пароля учетной записи пользователя истекает.

</dd> <dt>

**пассвордрекуиред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры управления сетью " \| [**\_ сведения о пользователе \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **УФ \_ PASSWD \_ нотрекд**")
</dt> </dl>

если задано **значение true**, то для учетной записи пользователя Windows требуется пароль. Если задано **значение false**, то для этой учетной записи пароль не требуется.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| идентификаторы безопасности Win32API (SID)")
</dt> </dl>

Идентификатор безопасности (SID) для этой учетной записи. Идентификатор безопасности — это строковое значение переменной длины, используемое для распознавания доверенного лица. каждая учетная запись имеет уникальный идентификатор безопасности, который имеет такой же центр, как Windowsный домен. Идентификатор безопасности хранится в базе данных безопасности. когда пользователь входит в систему, система получает sid пользователя из базы данных, помещает идентификатор безопасности в маркер доступа пользователя, а затем использует идентификатор безопасности в маркере доступа пользователя для обнаружения пользователя во всех последующих взаимодействиях с Windows безопасностью. Каждый идентификатор безопасности является уникальным идентификатором для пользователя или группы, а другой пользователь или группа не могут иметь одинаковый идентификатор безопасности.

Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).

</dd> <dt>

**Идентификатор типа безопасности**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| управления доступом для типов перечисления \| [**SID \_ \_ use**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")
</dt> </dl>

Перечислимое значение, указывающее тип идентификатора безопасности.

Это свойство наследуется [**от \_ учетной записи Win32**](win32-account.md).

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**Сидтипеусер** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**Сидтипеграуп** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**Сидтипедомаин** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**Сидтипеалиас** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**Сидтипевеллкновнграуп** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**Сидтипеделетедаккаунт** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**Сидтипеинвалид** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**Сидтипеункновн** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**Сидтипекомпутер** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. В число рабочих состояний входят: "ОК", "пониженное состояние" и "пред-ошибка" — такой элемент, как жесткий диск с поддержкой SMART, который может работать должным образом, но прогнозирует сбой в ближайшем будущем. Нерабочие состояния: "ошибка", "Запуск", "остановка" и "служба", которые могут применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.

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

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ UserAccount** является производным от [**\_ учетной записи Win32**](win32-account.md).

> [!Note]  
> Ошибка не возвращается для попытки записи в свойство, доступное только для чтения, и значение свойства остается неизменным.

 

## <a name="examples"></a>Примеры

Пример " [список локальных учетных записей пользователей с помощью инструментария WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript" в коллекции TechNet использует **Win32 \_ UserAccount** для возврата сведений о локальных учетных записях пользователей, найденных на компьютере.

[Преобразование SID в учетную запись пользователя и учетную запись пользователя в sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) Пример кода PowerShell в коллекции TechNet использует **Win32 \_ UserAccount** для преобразования идентификатора безопасности в учетную запись пользователя и (или) учетную запись пользователя в идентификатор безопасности.

В следующем примере кода VBScript показано, как получить полное имя пользователя на локальном компьютере. Полное имя — это имя человека, например, пользователь может иметь имя «кенсанчез», а полное имя — «Алексей Sanchez)», поэтому вы можете подставить реальное имя домена и имя пользователя для «Мидомаиннаме» и «MyUserName». Для эффективного запроса необходимо указать и свойства домена, и имя пользователя.

Если вы являетесь администратором на удаленном компьютере, можно назначить имя удаленного компьютера для strComputer (вместо "."), а затем использовать сценарий следующего типа, чтобы получить полное имя учетной записи пользователя на локальном компьютере — с удаленного компьютера.


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
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

[**\_Учетная запись Win32**](win32-account.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 

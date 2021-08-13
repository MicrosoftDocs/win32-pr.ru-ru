---
description: '&Win32 \_ дкомаппликатионсеттинг \# 8194; Класс WMI представляет параметры DCOM-приложения.'
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Класс Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b52ace8ea72d78585ac0df858df1fc807fbc65ca74ace92208d2e9fc5c76861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417736"
---
# <a name="win32_dcomapplicationsetting-class"></a>\_Класс Win32 дкомаппликатионсеттинг

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дкомаппликатионсеттинг для Win32** представляет параметры DCOM-приложения. В нем содержатся параметры конфигурации DCOM, связанные с ключом **AppID** в реестре. Эти параметры действительны для компонентов, логически сгруппированных в данном классе приложения.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ дкомаппликатионсеттинг** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ дкомаппликатионсеттинг** содержит следующие методы.



| Метод                                                                                                                        | Описание                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетакцесссекуритидескриптор**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Возвращает дескриптор безопасности, управляющий доступом к приложению DCOM.<br/>                                                                                                                              |
| [**жетконфигуратионсекуритидескриптор**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Возвращает дескриптор безопасности, определяющий, кому разрешено настраивать DCOM-приложение.<br/>                                                                                                                           |
| [**жетлаунчсекуритидескриптор**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Возвращает дескриптор безопасности, определяющий, кому разрешено запускать DCOM-приложение.<br/>                                                                                                                              |
| [**сетакцесссекуритидескриптор**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |
| [**сетконфигуратионсекуритидескриптор**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Обновляет дескриптор безопасности конфигурации приложения DCOM с помощью нового дескриптора безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/> |
| [**сетлаунчсекуритидескриптор**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Обновляет дескриптор безопасности запуска приложения DCOM с помощью нового дескриптора безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ дкомаппликатионсеттинг** имеет следующие свойства.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ . \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] ")
</dt> </dl>

Глобальный уникальный идентификатор (GUID) для этого DCOM-приложения.

</dd> <dt>

**аусентикатионлевел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ аусентикатионлевел \] ")
</dt> </dl>

Минимальный уровень проверки подлинности клиента, необходимый для этого COM-сервера. Если **значение равно NULL**, используются значения по умолчанию.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (1)


</dt> <dd>

Нет (проверка подлинности не выполняется)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Подключение** (2)


</dt> <dd>

Подключение (проверка подлинности выполняется только в том случае, если клиент устанавливает связь с приложением)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Вызов** (3)


</dt> <dd>

Вызов (проверка подлинности выполняется только в начале каждого вызова, когда приложение получает запрос)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Пакет** (4)


</dt> <dd>

Пакет (проверка подлинности выполняется для всех данных, полученных от клиента).

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**Паккетинтегрити** (5)


</dt> <dd>

Паккетинтегрити (все данные, передаваемые между клиентом и приложением, проходят проверку подлинности и проверяются)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**Паккетприваци** (6)


</dt> <dd>

Паккетприваци (используются свойства других уровней проверки подлинности, и все данные шифруются)

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

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**кустомсуррогате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ дллсуррогате \] ")
</dt> </dl>

Имя пользовательского суррогата, в котором активируется внутрипроцессный DCOM-приложение. Если это значение равно **null** , а ключ **Усесуррогате** имеет **значение true**, система предоставляет суррогатный процесс.

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

**енаблеатсторажеактиватион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ активатеатстораже \] ")
</dt> </dl>

DCOM-приложение получает сохраненное состояние приложения или начинается с состояния, в котором сначала инициализируется приложение.

</dd> <dt>

**локальная служба.**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ программные классы на локальном компьютере \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Имя для служб, предоставляемых приложением DCOM.

</dd> <dt>

**ремотесервернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ремотесервернаме \] ")
</dt> </dl>

Имя удаленного сервера, на котором активировано приложение.

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ . \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ AppID \\ \\ {GUID} \[ runas \] ")
</dt> </dl>

Учетная запись конкретного пользователя, под которой приложение должно запускаться при активации.

</dd> <dt>

**сервицепараметерс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ сервицепараметерс \] ")
</dt> </dl>

Параметры командной строки, передаваемые в DCOM-приложение. это допустимо только в том случае, если приложение написано как служба на основе Windows.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**усесуррогате**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ дллсуррогате \] ")
</dt> </dl>

DCOM-приложение может быть активировано как сервер вне процесса с помощью суррогатного исполняемого файла.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ дкомаппликатионсеттинг** является производным от [**Win32 \_ комсеттинг**](win32-comsetting.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Комсеттинг Win32**](win32-comsetting.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 


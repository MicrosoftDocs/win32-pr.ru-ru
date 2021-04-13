---
title: Класс Win32_TSDiscoveredLicenseServer
description: Предоставляет сведения об обнаруженном сервере лицензирования удаленный рабочий стол.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSDiscoveredLicenseServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSDiscoveredLicenseServer, описание
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492717"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a>\_Класс Win32 тсдисковередлиценсесервер

Предоставляет сведения об обнаруженном сервере лицензирования удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсдисковередлиценсесервер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсдисковередлиценсесервер** имеет следующие свойства.

<dl> <dt>

**ховдисковеред**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Это свойство более не поддерживается.

**Windows Server 2008:** Метод обнаружения сервера лицензий удаленный рабочий стол.

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**Граупполициконфигуред** (0)


</dt> <dd>

Сервер лицензирования обнаружен с помощью групповой политики.

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**Регистриконфигуред** (1)


</dt> <dd>

Сервер лицензирования обнаружен с помощью параметра реестра.

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**Воркграупдисковери** (2)


</dt> <dd>

Сервер лицензирования обнаружен с помощью области обнаружения рабочих групп.

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**Домаиндисковери** (3)


</dt> <dd>

Сервер лицензирования обнаружен с помощью области обнаружения доменов.

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**Ентерприседисковери** (4)


</dt> <dd>

Сервер лицензирования обнаружен с помощью области обнаружения в лесах.

</dd> </dl>

</dd> <dt>

**исадминонлс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, имеет ли учетная запись, используемая для запуска скрипта или EXE-файла, использование класса **Win32 \_ тсдисковередлиценсесервер** , доступ администратора к серверу лицензирования.

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span id="No"></span><span id="no"></span><span id="NO"></span>**Нет** (0)


</dt> <dd>

Используемая учетная запись не имеет прав администратора на доступ к серверу лицензирования.

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Да** (1)


</dt> <dd>

Используемая учетная запись имеет права администратора для доступа к серверу лицензирования.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Не, знание** (2)


</dt> <dd>

Невозможно определить, имеет ли используемая учетная запись права администратора для доступа к серверу лицензирования.

</dd> </dl>

</dd> <dt>

**ислсаваилабле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, доступен ли сервер лицензирования (удаленно ли RPC-подключение удаленного вызова процедур \[ \] к серверу).

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)


</dt> <dd>

Сервер лицензирования недоступен.

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (1)


</dt> <dd>

Сервер лицензирования доступен.

</dd> </dl>

</dd> <dt>

**иссуингкалс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли серверу лицензирования выдавать службы удаленных рабочих столов клиентские лицензии RDS на сервер узла сеансов удаленных рабочих столов.

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Не разрешено** (0)


</dt> <dd>

Серверу лицензирования не разрешено выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Разрешено** (1)


</dt> <dd>

Серверу лицензирования разрешено выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Не, знание** (2)


</dt> <dd>

Невозможно определить, может ли сервер лицензирования выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.

</dd> </dl>

</dd> <dt>

**лиценсесервер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя обнаруженного сервера лицензирования удаленный рабочий стол.

</dd> </dl>

## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 


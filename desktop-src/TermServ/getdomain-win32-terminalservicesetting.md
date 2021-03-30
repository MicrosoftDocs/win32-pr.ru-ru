---
title: Метод @ Domain класса Win32_TerminalServiceSetting
description: Возвращает имя домена, в который входит сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- Метод службы удаленных рабочих столов
- Метод службы удаленных рабочих столов, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод @ domain
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e9b2e5ba62f12c67a753cf8e5c41e8296b31e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988283"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a>Метод WebMethod \_ класса Win32 терминалсервицесеттинг

Возвращает имя домена, в который входит сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Домен* \[ заполняет\]
</dt> <dd>

Доменное имя сервера узла сеансов удаленных рабочих столов.

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
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


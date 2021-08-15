---
title: Метод Жетвинстатиондривернамес класса Win32_TerminalServiceSetting
description: Возвращает список имен драйверов Винстатион.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвинстатиондривернамес
- Службы удаленных рабочих столов метода Жетвинстатиондривернамес, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетвинстатиондривернамес
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d51d31e6a9857dd1ec1faf46df2adadc4379c0ccf99a7a5ed634a4fa27bf4d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059482"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a>Метод Жетвинстатиондривернамес \_ класса Win32 терминалсервицесеттинг

Возвращает список имен драйверов Винстатион.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Винстадривернамес* \[ заполняет\]
</dt> <dd>

Список имен драйверов Винстатион.

</dd> </dl>

## <a name="remarks"></a>Remarks

Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6. в следующем примере Visual Basic scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 


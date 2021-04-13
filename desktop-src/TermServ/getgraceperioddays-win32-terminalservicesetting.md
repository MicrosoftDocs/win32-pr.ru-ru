---
title: Метод Жетграцепериоддайс класса Win32_TerminalServiceSetting
description: Извлекает количество дней, оставшихся в службы удаленных рабочих столов льготный период лицензирования для сервера узла сеансов удаленный рабочий стол. Нулевое значение указывает, что льготный период истек.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетграцепериоддайс
- Службы удаленных рабочих столов метода Жетграцепериоддайс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетграцепериоддайс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340475"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Метод Жетграцепериоддайс \_ класса Win32 терминалсервицесеттинг

Извлекает количество дней, оставшихся в службы удаленных рабочих столов льготный период лицензирования для сервера узла сеансов удаленный рабочий стол. Нулевое значение указывает, что льготный период истек.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дайслефт* \[ заполняет\]
</dt> <dd>

Количество дней, оставшихся в льготном периоде.

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

 


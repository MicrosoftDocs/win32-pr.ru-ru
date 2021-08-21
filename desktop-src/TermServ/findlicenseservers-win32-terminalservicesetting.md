---
title: Метод Финдлиценсесерверс класса Win32_TerminalServiceSetting
description: Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Финдлиценсесерверс
- Службы удаленных рабочих столов метода Финдлиценсесерверс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Финдлиценсесерверс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98af0d63c736e5bc82dd13d2abc94786634d7b92ba2c9a4628ae8ffd32a18b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130793"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a>Метод Финдлиценсесерверс \_ класса Win32 терминалсервицесеттинг

Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лиценсесерверслист* \[ заполняет\]
</dt> <dd>

Список объектов [**Win32 \_ тсдисковередлиценсесервер**](win32-tsdiscoveredlicenseserver.md) . Каждый объект в списке выходных данных имеет имя сервера лицензирования удаленный рабочий стол и метод обнаружения.

</dd> <dt>

*Количество* \[ заполняет\]
</dt> <dd>

Общее число обнаруженных серверов лицензий удаленный рабочий стол в списке выходных данных.

</dd> </dl>

## <a name="remarks"></a>Remarks

Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6. в следующем примере Visual Basic scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


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

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


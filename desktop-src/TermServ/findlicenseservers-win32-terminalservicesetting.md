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
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989252"
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

 


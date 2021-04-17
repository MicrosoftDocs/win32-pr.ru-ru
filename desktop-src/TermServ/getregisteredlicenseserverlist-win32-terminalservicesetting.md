---
title: Метод Жетрегистередлиценсесерверлист класса Win32_TerminalServiceSetting
description: Возвращает список зарегистрированных серверов лицензирования.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетрегистередлиценсесерверлист
- Службы удаленных рабочих столов метода Жетрегистередлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетрегистередлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682084"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Метод Жетрегистередлиценсесерверлист \_ класса Win32 терминалсервицесеттинг

Возвращает список зарегистрированных серверов лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Регистередлслист* \[ заполняет\]
</dt> <dd>

Массив строк, который получает список зарегистрированных серверов лицензирования. Если нет зарегистрированных серверов лицензирования, этот массив будет пустым.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 






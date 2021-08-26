---
title: Метод Сетпримарилиценсесервер класса Win32_TerminalServiceSetting
description: Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпримарилиценсесервер
- Службы удаленных рабочих столов метода Сетпримарилиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетпримарилиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42eee8bbcab6494459ddde5c339f3836cab414ad3c2f5204399bac09e362c3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008924"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Метод Сетпримарилиценсесервер \_ класса Win32 терминалсервицесеттинг

Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лиценсесервернаме* \[ окне\]
</dt> <dd>

Имя сервера лицензирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 






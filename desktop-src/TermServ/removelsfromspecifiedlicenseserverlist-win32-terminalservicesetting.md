---
title: Метод РемовелсфромспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода РемовелсфромспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода РемовелсфромспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод РемовелсфромспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 492b955b8aced6972ec80f499af5ca4b043141159ad2c8fd359225302d8f63b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605193"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Метод РемовелсфромспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг

Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лиценсесервернаме* \[ окне\]
</dt> <dd>

Имя удаляемого сервера лицензирования.

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
</dt> <dt>

[**аддлстоспеЦифиедлиценсесерверлист**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**емптиспеЦифиедлиценсесерверлист**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**жетспеЦифиедлиценсесерверлист**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**сетспеЦифиедлиценсесерверлист**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






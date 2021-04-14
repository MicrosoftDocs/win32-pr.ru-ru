---
title: Метод ЖетспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Извлекает список указанных серверов лицензирования.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ЖетспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода ЖетспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод ЖетспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414924"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Метод ЖетспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг

Извлекает список указанных серверов лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*СпеЦифиедлслист* \[ заполняет\]
</dt> <dd>

Массив строк, который получает список серверов лицензирования. Если серверы лицензий отсутствуют, этот массив будет пустым.

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

[**ремовелсфромспеЦифиедлиценсесерверлист**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**сетспеЦифиедлиценсесерверлист**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






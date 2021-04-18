---
title: Метод СетспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода СетспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод СетспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681962"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Метод СетспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг

Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*СпеЦифиедлслист* \[ окне\]
</dt> <dd>

Массив строк, содержащий новый список указанных серверов лицензирования.

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

[**жетспеЦифиедлиценсесерверлист**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**емптиспеЦифиедлиценсесерверлист**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**ремовелсфромспеЦифиедлиценсесерверлист**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






---
title: Метод Упдатедиректконнектлиценсесервер класса Win32_TerminalServiceSetting
description: Упдатедиректконнектлиценсесервер больше не доступен.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Упдатедиректконнектлиценсесервер
- Службы удаленных рабочих столов метода Упдатедиректконнектлиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Упдатедиректконнектлиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672677"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Метод Упдатедиректконнектлиценсесервер \_ класса Win32 терминалсервицесеттинг

\[**Упдатедиректконнектлиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]

**Windows Server 2008:** Обновляет список серверов лицензирования обнаружения. Список серверов отделяется точкой с запятой (";").

## <a name="syntax"></a>Синтаксис


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лиценсесерверлист* \[ окне\]
</dt> <dd>

Список серверов лицензирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                               |
| Поддержка конца сервера<br/>    | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


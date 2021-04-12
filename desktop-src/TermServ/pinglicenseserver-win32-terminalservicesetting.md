---
title: Метод Пинглиценсесервер класса Win32_TerminalServiceSetting
description: Пинглиценсесервер больше не доступен.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Пинглиценсесервер
- Службы удаленных рабочих столов метода Пинглиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Пинглиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415449"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Метод Пинглиценсесервер \_ класса Win32 терминалсервицесеттинг

\[**Пинглиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]

**Windows Server 2008:** Проверяет связь сервера лицензирования с сервером лицензий, чтобы определить, является ли он допустимым сервером лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя сервера* \[ окне\]
</dt> <dd>

Имя сервера лицензирования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

<dl> <dt>

**\_ОК**
</dt> <dd>

Сервер является действительным сервером лицензирования.

</dd> <dt>

**S \_ false**
</dt> <dd>

Недопустимый сервер лицензирования.

</dd> </dl>

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

 


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
ms.openlocfilehash: 4e5a52268073a076c5dada44b7f34c6a6b3e0c820c0b9819f65d23081f4f6c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866104"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Метод Пинглиценсесервер \_ класса Win32 терминалсервицесеттинг

\[**пинглиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]

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

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                               |
| Поддержка конца сервера<br/>    | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 


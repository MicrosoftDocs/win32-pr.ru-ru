---
title: Метод Сетброкернонхамоде класса Win32_SessionBrokerServiceProperties
description: Переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетброкернонхамоде
- Службы удаленных рабочих столов метода Сетброкернонхамоде, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетброкернонхамоде
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681881"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Сетброкернонхамоде \_ класса Win32 сессионброкерсервицепропертиес

Переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*коннстрингтоцентралдбрдкмс* \[ окне\]
</dt> <dd>

Строка подключения к центральной базе данных.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сессионброкерсервицепропертиес Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






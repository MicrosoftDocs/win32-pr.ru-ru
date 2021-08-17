---
title: Метод Сетброкернонхамоде класса Win32_SessionBrokerServiceProperties
description: переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.
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
ms.openlocfilehash: 34daa0817056975a6b15164dd29edcbcc86cd7cd9475f753e91500845ce089a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058413"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Сетброкернонхамоде \_ класса Win32 сессионброкерсервицепропертиес

переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.

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

 

 






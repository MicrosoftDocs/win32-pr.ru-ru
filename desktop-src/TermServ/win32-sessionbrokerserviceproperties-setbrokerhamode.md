---
title: Метод Сетброкерхамоде класса Win32_SessionBrokerServiceProperties
description: Переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server. Он также настраивает сервер брокера для использования центрального SQL Server.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетброкерхамоде
- Службы удаленных рабочих столов метода Сетброкерхамоде, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетброкерхамоде
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135894"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Сетброкерхамоде \_ класса Win32 сессионброкерсервицепропертиес

Переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server. Он также настраивает сервер брокера для использования центрального SQL Server.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*коннстрингтоцентралдбрдкмс* \[ окне\]
</dt> <dd>

Строка подключения к центральной базе данных.

</dd> <dt>

*секондариконнстрингтоцентралдбрдкмс* \[ окне\]
</dt> <dd>

Вторичная строка подключения к центральной базе данных.

**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.

</dd> <dt>

*брокерднсррнаме* \[ окне\]
</dt> <dd>

Имя DNS компонента Service Broker.

</dd> <dt>

*активеброкернаме* \[ окне\]
</dt> <dd>

Имя активного брокера.

**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.

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

 

 






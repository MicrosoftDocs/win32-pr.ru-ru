---
title: Метод Исдбреачабле класса Win32_SessionBrokerServiceProperties
description: Проверяет доступность базы данных.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Исдбреачабле
- Службы удаленных рабочих столов метода Исдбреачабле, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Исдбреачабле
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490581"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Исдбреачабле \_ класса Win32 сессионброкерсервицепропертиес

Проверяет доступность базы данных.

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*коннстрингтодб* \[ окне\]
</dt> <dd>

Строка подключения к базе данных.

</dd> <dt>

*коннсекондаристрингтодб* \[ окне\]
</dt> <dd>

Вторичная строка подключения к центральной базе данных.

**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.

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

 

 






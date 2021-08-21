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
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848421"
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

**Windows Server 2012 R2 и Windows Server 2012:** Этот параметр недоступен до Windows Server 2016.

</dd> <dt>

*активеброкернаме* \[ окне\]
</dt> <dd>

Имя активного брокера.

**Windows Server 2012 R2 и Windows Server 2012:** Этот параметр недоступен до Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Сессионброкерсервицепропертиес Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






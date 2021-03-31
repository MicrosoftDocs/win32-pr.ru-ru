---
title: Метод Инсталлброкердатабасе класса Win32_SessionBrokerServiceProperties
description: Устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном сервере SQL Server.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлброкердатабасе
- Службы удаленных рабочих столов метода Инсталлброкердатабасе, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Инсталлброкердатабасе
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801300"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Инсталлброкердатабасе \_ класса Win32 сессионброкерсервицепропертиес

Устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном сервере SQL Server.

## <a name="syntax"></a>Синтаксис


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*невдбфилепас* \[ окне\]
</dt> <dd>

путь к файлу новой базы данных.

</dd> <dt>

*коннстрингтоцентралдбмастер* \[ окне\]
</dt> <dd>

Строка подключения к главному хозяину базы данных.

</dd> <dt>

*централрдкмсдбнаме* \[ окне\]
</dt> <dd>

Имя центральной базы данных.

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

 

 






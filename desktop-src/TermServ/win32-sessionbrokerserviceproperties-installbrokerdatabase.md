---
title: Метод Инсталлброкердатабасе класса Win32_SessionBrokerServiceProperties
description: устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном SQL сервере.
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
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422454"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Инсталлброкердатабасе \_ класса Win32 сессионброкерсервицепропертиес

устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном SQL сервере.

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

## <a name="requirements"></a>Requirements (Требования)



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

 

 






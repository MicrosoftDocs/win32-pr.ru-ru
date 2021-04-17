---
title: Метод Сетсбдбконнектионстрингс класса Win32_SessionBrokerServiceProperties
description: Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсбдбконнектионстрингс
- Службы удаленных рабочих столов метода Сетсбдбконнектионстрингс, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетсбдбконнектионстрингс
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490578"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Сетсбдбконнектионстрингс \_ класса Win32 сессионброкерсервицепропертиес

Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*коннстрингтоцентралдбрдкмс* \[ окне\]
</dt> <dd>

Основная строка подключения.

</dd> <dt>

*секондариконнстрингтоцентралдбрдкмс* \[ окне\]
</dt> <dd>

Вторичная строка подключения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сессионброкерсервицепропертиес Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






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
ms.openlocfilehash: b89baa40d25e6ecf316ac6904cc89091fa581d87be1018c52fa31c2b7ab358d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058422"
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

 

 






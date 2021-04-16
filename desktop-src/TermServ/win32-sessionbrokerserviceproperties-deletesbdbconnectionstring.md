---
title: Метод Делетесбдбконнектионстринг класса Win32_SessionBrokerServiceProperties
description: Удаляет строки подключения к базе данных (первичной или вторичной) из реестра.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетесбдбконнектионстринг
- Службы удаленных рабочих столов метода Делетесбдбконнектионстринг, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Делетесбдбконнектионстринг
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672655"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Метод Делетесбдбконнектионстринг \_ класса Win32 сессионброкерсервицепропертиес

Удаляет строки подключения к базе данных (первичной или вторичной) из реестра.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Иссекондариконнстринг* \[ окне\]
</dt> <dd>

Если **значение — true**, вторичная строка подключения удаляется. Если **значение равно false**, то основная строка подключения удаляется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сессионброкерсервицепропертиес Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 






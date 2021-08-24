---
title: Метод Жетактивесервер класса Win32_RDMSEnvironment
description: Получает полное доменное имя (FQDN) среды служб управления удаленный рабочий стол (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетактивесервер
- Службы удаленных рабочих столов метода Жетактивесервер, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Жетактивесервер
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730fa1230ddf08f5bd598e2041cd82ab4287d30387fa61460771fea5bcf3ec50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139017"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Метод Жетактивесервер \_ класса Win32 рдмсенвиронмент

Получает полное доменное имя (FQDN) среды служб управления удаленный рабочий стол (RDMS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя сервера* \[ заполняет\]
</dt> <dd>

Получает полученное полное доменное имя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсенвиронмент Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 






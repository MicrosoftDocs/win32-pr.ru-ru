---
title: Метод Стартскавенгинг класса MicrosoftDNS_Server
description: Метод Стартскавенгинг запускает очистку устаревших записей в зонах, подлежащим очистке.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS-метод Стартскавенгинг
- Стартскавенгинг метода DNS, класс MicrosoftDNS_Server
- DNS класса MicrosoftDNS_Server, метод Стартскавенгинг
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988805"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Метод Стартскавенгинг \_ класса микрософтднс Server

Метод **стартскавенгинг** запускает очистку устаревших записей в зонах, подлежащим очистке.

## <a name="syntax"></a>Синтаксис


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Ошибка \_ указывает, что очистка успешно запущена. Любое другое значение является кодом ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сервер микрософтднс**](microsoftdns-server.md)
</dt> <dt>

[**Метод StartService \_ класса микрософтднс Server**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Метод работы \_ класса микрософтднс Server**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Метод Жетдистингуишеднаме \_ класса микрософтднс Server**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 






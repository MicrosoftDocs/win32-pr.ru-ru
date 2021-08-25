---
description: Возвращает идентификатор службы для проверки подлинности с помощью токена конечной точки.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Метод Иупдатиндпоинтаустокен:: ServiceID (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: fd7e15059db01062fae290d9c4da46a9ef07683acae9f2e58afe29830817c787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855794"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>Метод Иупдатиндпоинтаустокен:: ServiceID

Возвращает идентификатор службы для проверки подлинности с помощью токена конечной точки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псервицеид* \[ заполняет\]
</dt> <dd>

Идентификатор службы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . в противном случае возвращает код ошибки COM или Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>                   |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                |
| Заголовок<br/>                   | <dl> <dt>Упдатиндпоинтаус. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Упдатиндпоинтаус. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Упдатиндпоинтаус. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иупдатиндпоинтаустокен**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 





---
description: Возвращает XML-данные (переданные по каналу передачи), представляющие токен.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Метод Иупдатиндпоинтаустокен:: Токендата (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8189b439c6ed42b46410ef4c36d904276a78652370353758ee26a921880d2d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106485"
---
# <a name="iupdateendpointauthtokentokendata-method"></a>Метод Иупдатиндпоинтаустокен:: Токендата

Возвращает XML-данные (переданные по каналу передачи), представляющие токен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзтокендата* \[ заполняет\]
</dt> <dd>

XML-данные (передаваемые по каналу передачи), представляющие токен. Например, данные для маркера WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1 — это код SAML, который добавляется в запрос.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**иупдатиндпоинтаустокен**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 





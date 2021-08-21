---
description: Возвращает XML-формат неприсоединенной ссылки на токен.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Метод Иупдатиндпоинтаустокен:: Токенреференцеунаттачед (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 2dada627d6e2b8832f4317c47e54a9c4417e14b821f6cd84bce44d9f53c99aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049252"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>Метод Иупдатиндпоинтаустокен:: Токенреференцеунаттачед

Возвращает XML-формат неприсоединенной ссылки на токен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзтокенреференце* \[ заполняет\]
</dt> <dd>

Указатель на неприсоединенную ссылку на маркер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . в противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Remarks

Неприсоединенная ссылка указывает на рефереце (например, сигнитуре, который использует маркер), не находящийся в сообщении, где находится маркер.

## <a name="requirements"></a>Requirements (Требования)



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

 

 





---
description: Возвращает XML-формат присоединенной ссылки на токен.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Метод Иупдатиндпоинтаустокен:: Токенреференцеаттачед (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: eae5e616e8583e2a1da8f8aa0882ea25160faad3f064734620466a0353736efe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793864"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>Метод Иупдатиндпоинтаустокен:: Токенреференцеаттачед

Возвращает XML-формат присоединенной ссылки на токен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзтокенреференце* \[ заполняет\]
</dt> <dd>

Указатель на ссылку на присоединенный маркер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . в противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Remarks

Присоединенная ссылка указывает на рефереце (например, сигнитуре, который использует токен), который находится в том же сообщении, где находится маркер.

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

 

 





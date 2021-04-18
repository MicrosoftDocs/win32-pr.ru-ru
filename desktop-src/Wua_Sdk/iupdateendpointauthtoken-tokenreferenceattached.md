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
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682760"
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

При успешном выполнении возвращает значение **\_ ОК** . В противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Комментарии

Присоединенная ссылка указывает на рефереце (например, сигнитуре, который использует токен), который находится в том же сообщении, где находится маркер.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                   |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                |
| Header<br/>                   | <dl> <dt>Упдатиндпоинтаус. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Упдатиндпоинтаус. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Упдатиндпоинтаус. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иупдатиндпоинтаустокен**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701631"
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

При успешном выполнении возвращает значение **\_ ОК** . В противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Комментарии

Неприсоединенная ссылка указывает на рефереце (например, сигнитуре, который использует маркер), не находящийся в сообщении, где находится маркер.

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

 

 





---
title: Метод Ивмсекуребуффер Encrypt (Вмдрмсдк. h)
description: Метод Encrypt шифрует указатель данных.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Шифрование метода Windows Media Format
- Шифрование метода Windows Media Format, интерфейс Ивмсекуребуффер
- Интерфейс Ивмсекуребуффер интерфейса Windows Media Format, метод Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708601"
---
# <a name="iwmsecurebufferencrypt-method"></a>Метод Ивмсекуребуффер:: Encrypt

Метод **Encrypt** шифрует указатель данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псекуречаннел* \[ окне\]
</dt> <dd>

Указатель на интерфейс безопасного канала, содержащий указатель данных для шифрования.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Используйте этот метод для шифрования указателей на данные, чтобы их можно было отправлять через границы DLL.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**расшифровка;**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Интерфейс Ивмсекуребуффер**](iwmsecurebuffer.md)
</dt> </dl>

 

 






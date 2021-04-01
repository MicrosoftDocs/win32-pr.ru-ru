---
description: Возвращает ключ, используемый для шифрования исходящих сообщений, которые защищает маркер.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Метод Иупдатиндпоинтаустокен:: SigningKey (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072801"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a>Метод Иупдатиндпоинтаустокен:: SigningKey

Возвращает ключ, используемый для шифрования исходящих сообщений, которые защищает маркер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбкэй* \[ в, out\]
</dt> <dd>

Ключ, используемый для шифрования исходящих сообщений.

</dd> <dt>

*пкбкэйсизе* \[ в, out\]
</dt> <dd>

Размер ключа, на который ссылается *пбкэй* пареметер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение **\_ ОК** . В противном случае возвращает код ошибки COM или Windows.

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

 

 





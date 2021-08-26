---
description: Возвращает предпочтительный тип маркера проверки подлинности для конечной точки службы.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Метод Иупдатиндпоинтауспровидер:: Жетпреферредендпоинттокентипе (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994584"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Метод Иупдатиндпоинтауспровидер:: Жетпреферредендпоинттокентипе

Возвращает предпочтительный тип маркера проверки подлинности для конечной точки службы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*serviceId* \[ окне\]
</dt> <dd>

Определяет обновляемую службу.

</dd> <dt>

*endpointType* \[ окне\]
</dt> <dd>

Определяет тип конечной точки тнидед для подключения к службе.

</dd> <dt>

*улрекуестедтипес* \[ окне\]
</dt> <dd>

Идентифицирует ORed набор токенов, поддерживаемых конечной точкой.

</dd> <dt>

*пулпреферредтокентипес* \[ заполняет\]
</dt> <dd>

Укажите ORed набор предпочтительных типов токенов проверки подлинности. (Задайте значение 0, чтобы указать, что маркер проверки подлинности не требуется).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_При успешном выполнении возвращает значение ОК. в противном случае возвращает код ошибки COM или Windows.

## <a name="remarks"></a>Remarks

При возврате этого метода WUA выбирает тип токена из предпочтительных типов и передает его в параметр tokenType метода [**жетендпоинттокен**](iupdateendpointauthprovider-getendpointtoken.md) .

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

[**иупдатиндпоинтауспровидер**](iupdateendpointauthprovider.md)
</dt> <dt>

[**жетендпоинттокен**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 





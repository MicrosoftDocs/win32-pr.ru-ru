---
title: Метод Modify класса MicrosoftDNS_NSType
description: Метод Modify обновляет запись ресурса сервера имен (NS).
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_NSType класс
- MicrosoftDNS_NSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8adcebb06aa7d796b9d4c79282fe04ec9047d54a0be1c69a302fdcddf78ca34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573784"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a>Метод Modify \_ класса микрософтднс нстипе

Метод **Modify** обновляет запись ресурса сервера имен (NS).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Ншост* \[ в необязательное\]
</dt> <dd>

Полномочный узел для домена.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на измененный объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Любой параметр, не указанный, остается неизменным в измененной записи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Микрософтднс \_ птртипе**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






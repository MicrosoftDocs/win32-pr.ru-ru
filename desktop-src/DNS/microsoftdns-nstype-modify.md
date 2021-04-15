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
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493293"
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

## <a name="remarks"></a>Комментарии

Любой параметр, не указанный, остается неизменным в измененной записи.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Микрософтднс \_ птртипе**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Птртипе микрософтднс**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






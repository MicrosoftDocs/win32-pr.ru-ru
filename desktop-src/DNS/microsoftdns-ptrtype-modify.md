---
title: Метод Modify класса MicrosoftDNS_PTRType
description: Метод Modify обновляет запись ресурса указателя (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_PTRType класс
- MicrosoftDNS_PTRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988810"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Метод Modify \_ класса микрософтднс птртипе

Метод **Modify** обновляет запись ресурса указателя (PTR).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Птрдомаиннаме* \[ в необязательное\]
</dt> <dd>

Адрес имени домена записи PTR.

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

 

 






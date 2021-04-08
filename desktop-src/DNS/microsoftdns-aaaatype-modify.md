---
title: Метод Modify класса MicrosoftDNS_AAAAType
description: Метод Modify обновляет запись ресурса IPv6-адреса (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AAAAType класс
- MicrosoftDNS_AAAAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891949"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Метод Modify \_ класса микрософтднс аааатипе

Метод **Modify** обновляет запись ресурса IPv6-адреса (AAAA).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*IPv6Address* \[ в необязательное\]
</dt> <dd>

IPv6-адрес узла.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на новый объект.

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

[**Микрософтднс \_ аааатипе**](microsoftdns-aaaatype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Аааатипе микрософтднс**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






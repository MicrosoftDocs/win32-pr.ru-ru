---
title: Метод Modify класса MicrosoftDNS_CNAMEType
description: Метод Modify обновляет запись ресурса канонического имени (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_CNAMEType класс
- MicrosoftDNS_CNAMEType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490653"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a>Метод Modify \_ класса микрософтднс кнаметипе

Метод **Modify** обновляет запись ресурса канонического имени (CNAME).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Примаринаме* \[ в необязательное\]
</dt> <dd>

Строка, представляющая основное имя записи CNAME.

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

[**Микрософтднс \_ кнаметипе**](microsoftdns-cnametype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Кнаметипе микрософтднс**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






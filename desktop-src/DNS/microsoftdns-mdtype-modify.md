---
title: Метод Modify класса MicrosoftDNS_MDType
description: Метод Modify обновляет запись ресурса почтового агента для домена (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MDType класс
- MicrosoftDNS_MDType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c402a753394c5ca7c12acf212377823a87d16e5d17f0d97981ab5e75d8a537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527264"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a>Метод Modify \_ класса микрософтднс мдтипе

Метод **Modify** обновляет запись ресурса почтового агента для домена (MD).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Мдхост* \[ в необязательное\]
</dt> <dd>

Строка, представляющая узел доставки почты.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на измененный объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

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

[**Микрософтднс \_ мдтипе**](microsoftdns-mdtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Мдтипе микрософтднс**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






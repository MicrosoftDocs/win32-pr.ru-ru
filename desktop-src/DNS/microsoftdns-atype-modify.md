---
title: Метод Modify класса MicrosoftDNS_AType
description: Метод Modify обновляет TTL и IP-адрес записи ресурса адреса узла (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_AType класс
- MicrosoftDNS_AType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d9f4740aeec92726796943e53b4d2143a6378341b061aaa7d3f3f6bf6dc7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163485"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Метод Modify \_ класса микрософтднс атипе

Метод **Modify** обновляет TTL и IP-адрес записи ресурса адреса узла (a).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*IP-адрес* \[ в необязательное\]
</dt> <dd>

Строка, представляющая IP-адрес узла.

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

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Атипе микрософтднс**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 






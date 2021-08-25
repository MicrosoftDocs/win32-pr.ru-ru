---
title: Метод Modify класса MicrosoftDNS_MGType
description: Метод Modify обновляет запись ресурса почтовой группы (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MGType класс
- MicrosoftDNS_MGType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db26f33e56ecc8553af1e34513a085b6eb6666ca99e2f91ec19383756094d6f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874914"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Метод Modify \_ класса микрософтднс мгтипе

Метод **Modify** обновляет запись ресурса почтовой группы (MG).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Мгмаилбокс* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик, который является членом почтовой группы, указанной в имени владельца записи.

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

[**Микрософтднс \_ мгтипе**](microsoftdns-mgtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Мгтипе микрософтднс**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






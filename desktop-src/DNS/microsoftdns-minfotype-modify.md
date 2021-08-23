---
title: Метод Modify класса MicrosoftDNS_MINFOType
description: Метод Modify обновляет запись ресурса почтовых сообщений (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MINFOType класс
- MicrosoftDNS_MINFOType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692564"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Метод Modify \_ класса микрософтднс минфотипе

Метод **Modify** обновляет запись ресурса почтовых сообщений (MINFO).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Респонсиблемаилбокс* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик, отвечающий за список рассылки или почтовый ящик, указанный в имени владельца записи.

</dd> <dt>

*Еррормаилбокс* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик для получения сообщений об ошибках, относящихся к списку рассылки, или к почтовому ящику, указанному именем владельца записи MINFO.

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

[**Микрософтднс \_ минфотипе**](microsoftdns-minfotype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Минфотипе микрософтднс**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






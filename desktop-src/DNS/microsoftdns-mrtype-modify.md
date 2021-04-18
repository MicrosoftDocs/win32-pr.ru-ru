---
title: Метод Modify класса MicrosoftDNS_MRType
description: Метод Modify обновляет запись ресурса переименования почтового ящика (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MRType класс
- MicrosoftDNS_MRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490485"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a>Метод Modify \_ класса микрософтднс мртипе

Метод **Modify** обновляет запись ресурса переименования почтового ящика (MR).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Мрмаилбокс* \[ окне\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик, который является правильным именем почтового ящика, указанного в имени владельца записи.

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

[**Микрософтднс \_ мртипе**](microsoftdns-mrtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Мртипе микрософтднс**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






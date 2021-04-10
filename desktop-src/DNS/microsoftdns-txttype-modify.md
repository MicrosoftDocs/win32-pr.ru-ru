---
title: Метод Modify класса MicrosoftDNS_TXTType
description: Метод Modify обновляет запись ресурса Text (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_TXTType класс
- MicrosoftDNS_TXTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135287"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Метод Modify \_ класса микрософтднс тксттипе

Метод **Modify** обновляет запись ресурса Text (txt).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Дескриптиветекст* \[ окне\]
</dt> <dd>

Описательный текст, семантика которого зависит от домена владельца.

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

[**Микрософтднс \_ тксттипе**](microsoftdns-txttype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Тксттипе микрософтднс**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






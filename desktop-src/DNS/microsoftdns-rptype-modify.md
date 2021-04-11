---
title: Метод Modify класса MicrosoftDNS_RPType
description: Метод Modify обновляет запись ресурса ответственного лица (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_RPType класс
- MicrosoftDNS_RPType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892118"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Метод Modify \_ класса микрософтднс рптипе

Метод **Modify** обновляет запись ресурса ответственного лица (RP).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Рпмаилбокс* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик ответственного лица.

</dd> <dt>

*Ткстдомаиннаме* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, для которого существуют записи ресурсов TXT.

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

[**Микрософтднс \_ рптипе**](microsoftdns-rptype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Рптипе микрософтднс**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






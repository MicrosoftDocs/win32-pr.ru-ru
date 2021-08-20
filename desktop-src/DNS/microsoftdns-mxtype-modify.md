---
title: Метод Modify класса MicrosoftDNS_MXType
description: Метод Modify обновляет запись ресурса почтового обменника (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_MXType класс
- MicrosoftDNS_MXType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fb31da6bf0861c94c54163fa9c771ac592fca105a5459214e17031c3b8e6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076788"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Метод Modify \_ класса микрософтднс мкстипе

Метод **Modify** обновляет запись ресурса почтового обменника (MR).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Настройка* \[ в необязательное\]
</dt> <dd>

Предпочтение данной записи ресурса между другими пользователями того же владельца. Более низкие значения являются предпочтительными.

</dd> <dt>

*Маилексчанже* \[ в необязательное\]
</dt> <dd>

Полное доменное имя с указанием узла, который будет использоваться в качестве почтового обмена для имени владельца.

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

[**Микрософтднс \_ мкстипе**](microsoftdns-mxtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






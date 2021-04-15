---
title: Метод Modify класса MicrosoftDNS_RTType
description: Метод Modify обновляет запись ресурса маршрута (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_RTType класс
- MicrosoftDNS_RTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534325"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Метод Modify \_ класса микрософтднс рттипе

Метод **Modify** обновляет запись ресурса маршрута (RT).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
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

*Интермедиатехост* \[ в необязательное\]
</dt> <dd>

Полное доменное имя, указывающее узел, который будет выступать в качестве промежуточного в достижение узла, указанного владельцем.

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

[**Микрософтднс \_ рттипе**](microsoftdns-rttype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Рттипе микрософтднс**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






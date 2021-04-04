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
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989330"
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

[**Микрософтднс \_ мкстипе**](microsoftdns-mxtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






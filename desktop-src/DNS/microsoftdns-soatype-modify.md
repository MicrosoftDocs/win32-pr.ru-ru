---
title: Метод Modify класса MicrosoftDNS_SOAType
description: Метод Modify обновляет запись ресурса начальной записи зоны (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_SOAType класс
- MicrosoftDNS_SOAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825084"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Метод Modify \_ класса микрософтднс соатипе

Метод **Modify** обновляет запись ресурса начальной записи зоны (SOA).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Серийный* \[ номер в необязательное\]
</dt> <dd>

Серийный номер SOA, представляющий количество обновлений зоны, используемых [*серверами-получателями*](s-gly.md) для определения необходимости передачи зоны.

</dd> <dt>

*Сервер* \[ в необязательное\]
</dt> <dd>

Имя сервера источника.

</dd> <dt>

*Респонсиблепарти* \[ в необязательное\]
</dt> <dd>

Адрес почтового ящика ответственного лица в виде псевдонима. домен, например xyz.microsoft.com. Обратите внимание на использование точки, а не символа @.

</dd> <dt>

*RefreshInterval* \[ в необязательное\]
</dt> <dd>

Время в секундах до обновления зоны, содержащей эту запись.

</dd> <dt>

*Ретриделай* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого DNS-сервер должен откладывать задержку между попытками разрешения имен.

</dd> <dt>

*Експирелимит* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого серверы-получатели должны ожидать ответа от сервера-источника, прежде чем отменять их копии файла зоны как недопустимые.

</dd> <dt>

*Минимумттл* \[ в необязательное\]
</dt> <dd>

Время жизни (в секундах), применяемое к записям ресурсов в зоне, которые не указывают собственный срок жизни.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на измененный объект

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

[**Микрософтднс \_ соатипе**](microsoftdns-soatype.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






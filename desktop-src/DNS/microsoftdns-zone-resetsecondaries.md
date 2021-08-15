---
title: Метод Ресетсекондариес класса MicrosoftDNS_Zone
description: Метод Ресетсекондариес сбрасывает IP-адреса для дополнительных DNS-серверов в зоне.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- DNS-метод Ресетсекондариес
- Ресетсекондариес метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Ресетсекондариес
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab3737bc8143f712560e5ea253237c97da4e2401b98886428642210805ca586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957293"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Метод Ресетсекондариес \_ класса зоны микрософтднс

Метод **ресетсекондариес** сбрасывает IP-адреса для дополнительных DNS-серверов в зоне.

## <a name="syntax"></a>Синтаксис


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Секондарисерверс* \[ окне\]
</dt> <dd>

Массив IP-адресов для дополнительных DNS-серверов.

</dd> <dt>

*Секуресекондариес* \[ окне\]
</dt> <dd>

Задает применяемый уровень безопасности и должен быть одним из следующих:

-   ЗОНА \_ сексекуре \_ без \_ безопасности
-   \_только зона сексекуре \_ NS \_
-   \_ \_ только список сексекуре \_ зоны
-   ЗОНА \_ сексекуре \_ No \_ ксфр

</dd> <dt>

*Нотифисерверс* \[ окне\]
</dt> <dd>

IP-адрес DNS-серверов для уведомления при изменении зоны.

</dd> <dt>

*Уведомление* \[ окне\]
</dt> <dd>

Параметр уведомления и должен иметь одно из следующих значений:

-   \_уведомление зоны \_ отключено
-   уведомление зоны для \_ \_ всех \_ получателей
-   \_только список уведомлений о зонах \_ \_

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR типа [**микрософтднс \_ Zone**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зона микрософтднс**](microsoftdns-zone.md)
</dt> <dt>

[**Метод Ажеаллрекордс \_ класса зоны микрософтднс**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Метод Чанжезонетипе \_ класса зоны микрософтднс**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Метод Креатезоне \_ класса зоны микрософтднс**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Метод Форцерефреш \_ класса зоны микрософтднс**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Метод Паусезоне \_ класса зоны микрософтднс**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Метод Релоадзоне \_ класса зоны микрософтднс**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Метод Ресумезоне \_ класса зоны микрософтднс**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Метод Упдатефромдс \_ класса зоны микрософтднс**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Метод Вритебаккзоне \_ класса зоны микрософтднс**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 






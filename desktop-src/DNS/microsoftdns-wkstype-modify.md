---
title: Метод Modify класса MicrosoftDNS_WKSType
description: Метод Modify обновляет запись ресурса Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WKSType класс
- MicrosoftDNS_WKSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892213"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Метод Modify \_ класса микрософтднс вкстипе

Метод **Modify** обновляет запись ресурса Well-Known Services (WKS).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Интернетаддресс* \[ в необязательное\]
</dt> <dd>

IP-адрес владельца записи.

</dd> <dt>

*Иппротокол* \[ в необязательное\]
</dt> <dd>

Строка, представляющая протокол IP для этой записи. Допустимые значения: UDP или TCP.

</dd> <dt>

*Службы* \[ в необязательное\]
</dt> <dd>

Строка, содержащая все службы, используемые записью службы хорошо известных служб (WKS).

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

[**Микрософтднс \_ вкстипе**](microsoftdns-wkstype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Вкстипе микрософтднс**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






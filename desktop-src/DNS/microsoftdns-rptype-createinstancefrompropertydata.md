---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_RPType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса ответственного лица (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_RPType
- DNS класса MicrosoftDNS_RPType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262198"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a>Метод Креатеинстанцефромпропертидата \_ класса Рптипе микрософтднс

Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса ответственного лица (RP).

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Днссервернаме* \[ окне\]
</dt> <dd>

FQDN или IP-адрес DNS-сервера, содержащего эту запись ресурса.

</dd> <dt>

*ContainerName* \[ окне\]
</dt> <dd>

Имя контейнера для экземпляра зоны, кэша или Русинтс, содержащего эту запись ресурса.

</dd> <dt>

*OwnerName* \[ окне\]
</dt> <dd>

Имя владельца для записи ресурса.

</dd> <dt>

*Рекордкласс* \[ в необязательное\]
</dt> <dd>

Класс записи ресурса. Значение по умолчанию — 1. Допустимы следующие значения.



| Значение                                                                                                | Значение                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | В (Интернет)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (КСНЕТ)<br/>    |
| <span id="3"></span><dl> <dt>**3-5**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**четырех**</dt> </dl> | HS (Хесиод)<br/>   |



 

</dd> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Рпмаилбокс* \[ окне\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик ответственного лица.

</dd> <dt>

*Ткстдомаиннаме* \[ окне\]
</dt> <dd>

Полное доменное имя, для которого существуют записи ресурсов TXT.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на новый объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

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

[**Метод Modify \_ класса микрософтднс рптипе**](microsoftdns-rptype-modify.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






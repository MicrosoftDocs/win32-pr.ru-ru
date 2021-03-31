---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_NXTType
description: Метод Креатеинстанцефромпропертидата создает экземпляр следующей записи ресурса (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_NXTType
- DNS класса MicrosoftDNS_NXTType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491415"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a>Метод Креатеинстанцефромпропертидата \_ класса Нксттипе микрософтднс

Метод **креатеинстанцефромпропертидата** создает экземпляр следующей записи ресурса (NXT).

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
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

*Некстдомаиннаме* \[ окне\]
</dt> <dd>

Следующее имя домена.

</dd> <dt>

*Типы* \[ окне\]
</dt> <dd>

Разделенный пробелами список назначенных пространств имен для имени владельца записи ресурса NXT.

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

[**Микрософтднс \_ нксттипе**](microsoftdns-nxttype.md)
</dt> <dt>

[**Метод Modify \_ класса микрософтднс нксттипе**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






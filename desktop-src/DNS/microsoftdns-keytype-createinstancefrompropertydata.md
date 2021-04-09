---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_KEYType
description: Метод Креатеинстанцефромпропертидата создает запись ресурса ключа.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_KEYType
- DNS класса MicrosoftDNS_KEYType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071991"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a>Метод Креатеинстанцефромпропертидата \_ класса KEYType микрософтднс

Метод **креатеинстанцефромпропертидата** создает запись ресурса ключа.

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
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

*Флаги* \[ окне\]
</dt> <dd>

Флаги, используемые для определения сопоставления, как описано в документе IETF RFC 2535.

</dd> <dt>

*Протокол* \[ окне\]
</dt> <dd>

Протокол, для которого можно использовать ключ, указанный в записи ресурса. Назначенные значения показаны в следующей таблице.



| Значение                                                                                                    | Значение                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | E-Mail<br/>        |
| <span id="3"></span><dl> <dt>**3-5**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**четырех**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Все протоколы<br/> |



 

</dd> <dt>

*Алгоритм* \[ окне\]
</dt> <dd>

Алгоритм, используемый с ключом, указанным в записи ресурса. Назначенные значения показаны в следующей таблице.



| Значение                                                                                                | Значение                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3-5**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**четырех**</dt> </dl> | Шифрование на основе эллиптических кривых<br/> |



 

</dd> <dt>

*PublicKey* \[ окне\]
</dt> <dd>

Открытый ключ, представленный в базовом 64, как описано в приложении A из RFC 2535.

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

[**Микрософтднс \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Метод Modify \_ класса микрософтднс KEYType**](microsoftdns-keytype-modify.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






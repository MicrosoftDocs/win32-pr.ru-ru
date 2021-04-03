---
title: Метод Modify класса MicrosoftDNS_KEYType
description: Метод Modify обновляет запись ресурса ключа.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_KEYType класс
- MicrosoftDNS_KEYType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137530"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Метод Modify \_ класса микрософтднс KEYType

Метод **Modify** обновляет запись ресурса ключа.

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Флаги, используемые для определения сопоставления, как описано в документе IETF RFC 2535.

</dd> <dt>

*Протокол* \[ в необязательное\]
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

*Алгоритм* \[ в необязательное\]
</dt> <dd>

Алгоритм, используемый с ключом, указанным в записи ресурса. Назначенные значения показаны в следующей таблице.



| Значение                                                                                                | Значение                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3-5**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**четырех**</dt> </dl> | Шифрование на основе эллиптических кривых<br/> |



 

</dd> <dt>

*PublicKey* \[ в необязательное\]
</dt> <dd>

Открытый ключ, представленный в базовом 64, как описано в приложении A из RFC 2535.

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

[**Микрософтднс \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса KEYType микрософтднс**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






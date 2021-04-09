---
title: Метод Modify класса MicrosoftDNS_SRVType
description: Метод Modify обновляет запись ресурса службы (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_SRVType класс
- MicrosoftDNS_SRVType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071955"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Метод Modify \_ класса микрософтднс срвтипе

Метод **Modify** обновляет запись ресурса службы (SRV).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Приоритет* \[ в необязательное\]
</dt> <dd>

Приоритет целевого узла, указанного в имени владельца. Более низкие значения подразумевают более высокие приоритеты.

</dd> <dt>

*Вес* \[ в необязательное\]
</dt> <dd>

Вес целевого узла. Это полезно при выборе между узлами с одинаковым приоритетом. Вероятность использования этого узла должна быть пропорциональна его весу.

</dd> <dt>

*Порт* \[ в необязательное\]
</dt> <dd>

Порт, используемый на целевом узле службы протокола.

</dd> <dt>

*Срвдомаиннаме* \[ в необязательное\]
</dt> <dd>

Полное доменное имя целевого узла. Целевой объект \\ . \\ означает, что служба не будет доступна в этом домене.

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

[**Микрософтднс \_ срвтипе**](microsoftdns-srvtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Срвтипе микрософтднс**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






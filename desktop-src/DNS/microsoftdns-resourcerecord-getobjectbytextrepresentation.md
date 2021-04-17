---
title: Метод Жетобжектбитекстрепресентатион класса MicrosoftDNS_ResourceRecord
description: Метод Жетобжектбитекстрепресентатион извлекает существующий экземпляр \_ класса Ресаурцерекорд микрософтднс.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS-метод Жетобжектбитекстрепресентатион
- Жетобжектбитекстрепресентатион метода DNS, класс MicrosoftDNS_ResourceRecord
- DNS класса MicrosoftDNS_ResourceRecord, метод Жетобжектбитекстрепресентатион
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491169"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс

Метод **жетобжектбитекстрепресентатион** извлекает существующий экземпляр класса [**\_ ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Синтаксис


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Днссервернаме* \[ окне\]
</dt> <dd>

Имя DNS-сервера, с которого должна быть получена запись ресурса.

</dd> <dt>

*ContainerName* \[ окне\]
</dt> <dd>

Имя контейнера, из которого должна быть получена запись ресурса.

</dd> <dt>

*Текстрепресентатион* \[ окне\]
</dt> <dd>

Текстовое представление извлекаемой записи ресурса.

</dd> <dt>

*RR* \[ заполняет\]
</dt> <dd>

Ссылка на созданную запись ресурса.

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

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 






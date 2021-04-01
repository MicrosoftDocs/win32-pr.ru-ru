---
title: Метод Креатеинстанцефромтекстрепресентатион класса MicrosoftDNS_ResourceRecord
description: Метод Креатеинстанцефромтекстрепресентатион создает экземпляр \_ объекта микрософтднс ресаурцерекорд.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS-метод Креатеинстанцефромтекстрепресентатион
- Креатеинстанцефромтекстрепресентатион метода DNS, класс MicrosoftDNS_ResourceRecord
- DNS класса MicrosoftDNS_ResourceRecord, метод Креатеинстанцефромтекстрепресентатион
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071733"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Метод Креатеинстанцефромтекстрепресентатион \_ класса Ресаурцерекорд микрософтднс

Метод **креатеинстанцефромтекстрепресентатион** создает экземпляр объекта [**микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Днссервернаме* \[ окне\]
</dt> <dd>

Имя DNS-сервера, на котором должна быть создана запись ресурса.

</dd> <dt>

*ContainerName* \[ окне\]
</dt> <dd>

Имя контейнера, в который следует поместить новую запись ресурса.

</dd> <dt>

*Текстрепресентатион* \[ окне\]
</dt> <dd>

Текстовое представление создаваемого экземпляра RR.

</dd> <dt>

*RR* \[ out, ref\]
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

[**Метод Жетобжектбитекстрепресентатион \_ класса Ресаурцерекорд микрософтднс**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 






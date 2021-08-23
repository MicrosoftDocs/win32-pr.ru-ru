---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MXType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтового обменника (MR).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MXType
- DNS класса MicrosoftDNS_MXType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad85168813abb9a5c92e77275d854050ad35256963d75b7f52792776be9a6e74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573920"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a>Метод Креатеинстанцефромпропертидата \_ класса Мкстипе микрософтднс

Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтового обменника (MR).

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
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
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Хесиод)<br/>   |



 

</dd> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Настройка* \[ окне\]
</dt> <dd>

Предпочтение данной записи ресурса между другими пользователями того же владельца. Более низкие значения являются предпочтительными.

</dd> <dt>

*Маилексчанже* \[ окне\]
</dt> <dd>

Полное доменное имя с указанием узла, который будет использоваться в качестве почтового обмена для имени владельца.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на новый объект.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Микрософтднс \_ мкстипе**](microsoftdns-mxtype.md)
</dt> <dt>

[**Метод Modify \_ класса микрософтднс мкстипе**](microsoftdns-mxtype-modify.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






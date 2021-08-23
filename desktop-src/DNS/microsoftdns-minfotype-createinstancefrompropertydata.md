---
title: Метод Креатеинстанцефромпропертидата класса MicrosoftDNS_MINFOType
description: Метод Креатеинстанцефромпропертидата создает экземпляр записи ресурса почтовых сведений (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- DNS-метод Креатеинстанцефромпропертидата
- Креатеинстанцефромпропертидата метода DNS, класс MicrosoftDNS_MINFOType
- DNS класса MicrosoftDNS_MINFOType, метод Креатеинстанцефромпропертидата
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce72838382dd5276a4a0b9b660b67f1d7f8cb04cb894c72f245e908a916ae8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573934"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a>Метод Креатеинстанцефромпропертидата \_ класса Минфотипе микрософтднс

Метод **креатеинстанцефромпропертидата** создает экземпляр записи ресурса почтовых сведений (MINFO).

## <a name="syntax"></a>Синтаксис


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
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

*Респонсиблемаилбокс* \[ окне\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик, отвечающий за список рассылки или почтовый ящик, указанный в имени владельца записи.

</dd> <dt>

*Еррормаилбокс* \[ окне\]
</dt> <dd>

Полное доменное имя, указывающее почтовый ящик для получения сообщений об ошибках, относящихся к списку рассылки, или к почтовому ящику, указанному именем владельца записи MINFO.

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

[**Микрософтднс \_ минфотипе**](microsoftdns-minfotype.md)
</dt> <dt>

[**Метод Modify \_ класса микрософтднс минфотипе**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






---
title: Метод Modify класса MicrosoftDNS_WINSType
description: Метод Modify обновляет запись ресурса службы Windows Internet Name Service (WINS).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WINSType класс
- MicrosoftDNS_WINSType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892218"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Метод Modify \_ класса микрософтднс винстипе

Метод **Modify** обновляет запись ресурса службы Windows Internet Name Service (WINS).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Маппингфлаг* \[ в необязательное\]
</dt> <dd>

Флаг сопоставления WINS, указывающий, следует ли включать запись в репликацию зоны. Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно. Допустимы следующие значения.



| Значение                                                                                                                                               | Значение                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Флаг репликации<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Флаг отсутствия репликации (локальная запись)<br/> |



 

</dd> <dt>

*Лукуптимеаут* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого DNS-сервер пытается выполнить разрешение с помощью поиска WINS.

</dd> <dt>

*CacheTimeout* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.

</dd> <dt>

*Винссерверс* \[ в необязательное\]
</dt> <dd>

Список разделенных запятыми IP-адресов WINS-серверов, используемых при поиске WINS.

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

[**Микрософтднс \_ винстипе**](microsoftdns-winstype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Винстипе микрософтднс**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






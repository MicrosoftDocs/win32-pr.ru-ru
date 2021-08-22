---
title: Метод Modify класса MicrosoftDNS_WINSRType
description: Метод Modify обновляет запись ресурса WINSR (WINSR) для просмотра WINS.
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_WINSRType класс
- MicrosoftDNS_WINSRType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076668"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Метод Modify \_ класса микрософтднс винсртипе

Метод **Modify** обновляет запись ресурса WINSR (WINSR) для просмотра WINS.

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
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

Флаг сопоставления WINSR, указывающий, следует ли включать запись в репликацию зоны. Он может иметь только два значения: 0x80000000 и 0x00010000, соответствующие флагам репликации и без репликации (локальная запись) соответственно.

</dd> <dt>

*Лукуптимеаут* \[ в необязательное\]
</dt> <dd>

Время ожидания (в секундах) для DNS-сервера, использующего обратный поиск WINS.

</dd> <dt>

*CacheTimeout* \[ в необязательное\]
</dt> <dd>

Время (в секундах), в течение которого DNS-сервер, использующий поиск WINS, может кэшировать ответ WINS-сервера.

</dd> <dt>

*Ресултдомаин* \[ в необязательное\]
</dt> <dd>

Имя домена, добавляемое к возвращенным NetBIOS-именам.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на новый объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Любой параметр, не указанный, остается неизменным в измененной записи.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Пространство имен<br/>                | Корневой \\ микрософтднс<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Днспров. mof</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Микрософтднс \_ винсртипе**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Винсртипе микрософтднс**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






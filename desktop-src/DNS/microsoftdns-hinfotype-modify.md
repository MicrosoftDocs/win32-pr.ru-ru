---
title: Метод Modify класса MicrosoftDNS_HINFOType
description: Метод Modify обновляет запись ресурса сведения об узле (HINFO).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_HINFOType класс
- MicrosoftDNS_HINFOType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344177f0e0a18da22294faef24a6d1c4e61598b4b5e8a804081bdd3a592cf440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984644"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Метод Modify \_ класса микрософтднс хинфотипе

Метод **Modify** обновляет запись ресурса сведения об узле (HINFO).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*ЦП* \[ в необязательное\]
</dt> <dd>

Тип ЦП владельца записи.

</dd> <dt>

*Операционная система* \[ в необязательное\]
</dt> <dd>

Операционная система владельца записи.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Ссылка на новый объект.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

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

[**Микрософтднс \_ хинфотипе**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Хинфотипе микрософтднс**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






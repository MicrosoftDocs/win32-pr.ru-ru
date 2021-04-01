---
title: Метод Modify класса MicrosoftDNS_ATMAType
description: Метод Modify обновляет запись ресурса ATM Address to Name (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_ATMAType класс
- MicrosoftDNS_ATMAType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071636"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Метод Modify \_ класса микрософтднс атматипе

Метод **Modify** обновляет запись ресурса ATM Address to Name (ATMA).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Формат* \[ в необязательное\]
</dt> <dd>

Формат адреса ATM. ФОРМАТ имеет два возможных значения: 0, указывающий формат адреса конечной системы (АЕСА) ATM, а 1 — формат E. 164.

</dd> <dt>

*Атмаддресс* \[ в необязательное\]
</dt> <dd>

Строка переменной длины октетов, содержащая ATM-адрес узла или владельца, к которому относится эта запись ресурса. Первые четыре байта массива используются для хранения размера строки октета. Наиболее значимый байт хранится в байте 0.

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

[**Микрософтднс \_ атматипе**](microsoftdns-atmatype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Атматипе микрософтднс**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






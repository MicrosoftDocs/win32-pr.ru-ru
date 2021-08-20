---
title: Метод Modify класса MicrosoftDNS_NXTType
description: Метод Modify обновляет следующую запись ресурса (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Изменение метода DNS
- Изменение метода DNS, MicrosoftDNS_NXTType класс
- MicrosoftDNS_NXTType класса DNS, метод Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163205"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Метод Modify \_ класса микрософтднс нксттипе

Метод **Modify** обновляет следующую запись ресурса (NXT).

## <a name="syntax"></a>Синтаксис


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Срок жизни* \[ в необязательное\]
</dt> <dd>

Время в секундах, в течение которого запись ресурса может быть кэширована распознавателем DNS.

</dd> <dt>

*Некстдомаиннаме* \[ окне\]
</dt> <dd>

Следующее имя домена.

</dd> <dt>

*Типы* \[ окне\]
</dt> <dd>

Разделенный пробелами список назначенных пространств имен для имени владельца записи ресурса NXT.

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

[**Микрософтднс \_ нксттипе**](microsoftdns-nxttype.md)
</dt> <dt>

[**Метод Креатеинстанцефромпропертидата \_ класса Нксттипе микрософтднс**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Микрософтднс \_ ресаурцерекорд**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






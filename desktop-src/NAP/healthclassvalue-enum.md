---
title: Перечисление Хеалсклассвалуе (Наппротокол. h)
description: Указывает значение TLV класса работоспособности.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Хеалсклассвалуе перечисление NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76b3fef268417f14bf22d2e25539a245cebc31820b746847f1e7b1091492b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891644"
---
# <a name="healthclassvalue-enumeration"></a>Перечисление Хеалсклассвалуе

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Тип перечисления **хеалсклассвалуе** указывает значение TLV класса работоспособности.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**хеалсклассфиревалл**
</dt> <dd>

TLV класса работоспособности — брандмауэр.

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**хеалскласспатчлевел**
</dt> <dd>

В TLV класса работоспособности находится уровень обновления.

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**хеалсклассантивирус**
</dt> <dd>

TLV класса работоспособности — это антивирусная программа.

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**хеалскласскритикалупдате**
</dt> <dd>

TLV класса работоспособности является критическим обновлением.

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**хеалсклассресервед**
</dt> <dd>

Зарезервировано только для системного использования.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |



 

 






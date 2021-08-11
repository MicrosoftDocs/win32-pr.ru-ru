---
title: Перечисление MPTHREAT_TYPE (Мпклиент. h)
description: Возможные типы угроз.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE перечисления устаревших Windows компонентов среды
- PMPTHREAT_TYPEные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858501603b67451db9b565609d0c263040d2186cf44d91646e6df6ce3871ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247145"
---
# <a name="mpthreat_type-enumeration"></a>\_Перечисление типов мпсреат

Возможные типы угроз.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**\_тип мпсреат \_ кновнбад**
</dt> <dd>

Обнаружена известная неплохая угроза с помощью сигнатуры.

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_поведение типа \_ мпсреат**
</dt> <dd>

Обнаружена подозрительная угроза с помощью мониторинга поведения.

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_неизвестный тип мпсреат \_**
</dt> <dd>

Неизвестные угрозы (Неклассифицированные).

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**\_тип мпсреат \_ кновнгуд**
</dt> <dd>

Известная хорошая угроза.

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**МПСРЕАТ \_ тип \_ NIS**
</dt> <dd>

Обнаружение угроз NIS.

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**МПСРЕАТ \_ тип \_ MaxValue**
</dt> <dd>

Максимально возможное значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 






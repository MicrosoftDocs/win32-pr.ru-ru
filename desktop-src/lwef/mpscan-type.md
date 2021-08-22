---
title: Перечисление MPSCAN_TYPE (Мпклиент. h)
description: Тип выполняемого сканирования.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE перечисления устаревших Windows компонентов среды
- PMPSCAN_TYPEные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747135"
---
# <a name="mpscan_type-enumeration"></a>\_Перечисление типов мпскан

Тип выполняемого сканирования.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_неизвестный тип мпскан \_**
</dt> <dd>

Только для внутреннего применения.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**\_Быстрый ввод типа мпскан \_**
</dt> <dd>

Сканирует выполняющиеся процессы и различные точки АВТОЗАПУСКА в системе, где обычно скрываются вредоносные программы.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**\_тип мпскан \_ Full**
</dt> <dd>

Выполняет быструю проверку, а затем проверяет все фиксированные диски системы.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_ресурс типа \_ мпскан**
</dt> <dd>

Сканирует определенные ресурсы, например файлы или папки.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**МПСКАН \_ тип \_ MaxValue**
</dt> <dd>

Максимально возможное значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 






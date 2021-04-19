---
description: Задает уровень принудительной операции защиты от потери данных в конечной точке.
title: Перечисление Длпаппенфорцелевел (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495953"
---
# <a name="dlpappenforcelevel-enumeration"></a>Перечисление Длпаппенфорцелевел

Задает уровень принудительной операции защиты от потери данных в конечной точке.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Константы

<dl> <dt>

*Длпаппенфорцелевелноне* \[ окне\]
</dt> <dd>

Приложение не принудительно применено. Система DLP принудительно применит операцию.

</dd> </dl>

<dl> <dt>

*Длпаппенфорцелевелнотифи* \[ окне\]
</dt> <dd>

Приложение кнопка будет использовать API DLP для уведомления системы DLP об операции. Система DLP принудительно применит операцию.

</dd> </dl>

<dl> <dt>

*Длпаппенфорцелевелпревент* \[ окне\]
</dt> <dd>

Не поддерживается в текущей версии.

</dd> </dl>

<dl> <dt>

*Длпаппенфорцелевелфулл* \[ окне\]
</dt> <dd>

Не поддерживается в текущей версии.

</dd> </dl>

<dl> <dt>

*Длпаппенфорцелевелкаунт* \[ окне\]
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>



## <a name="remarks"></a>Remarks

Значения из этого перечисления используются структурой [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |


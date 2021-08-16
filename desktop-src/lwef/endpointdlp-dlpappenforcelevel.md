---
description: Задает уровень принудительной операции защиты от потери данных в конечной точке.
title: Перечисление DlpAppEnforceLevel (endpointdlp.h)
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
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349354"
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


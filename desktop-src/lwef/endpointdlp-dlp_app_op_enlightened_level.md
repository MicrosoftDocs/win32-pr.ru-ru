---
description: Связывает действие защиты от потери данных (DLP) конечной точки с уровнем применения.
title: Структура DLP_APP_OP_ENLIGHTENED_LEVEL (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495965"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>Структура DLP_APP_OP_ENLIGHTENED_LEVEL

Связывает действие защиты от потери данных (DLP) конечной точки с уровнем применения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Члены

<dl> <dt>

*Операция* \[ окне\]
</dt> <dd>

Значение из перечисления [длпактионтипе](endpointdlp-dlpactiontype.md) , указывающее тип действия DLP конечной точки.

</dd> </dl>

<dl> <dt>

*Аппенфорцементлевел* \[ окне\]
</dt> <dd>

Значение из [длпаппенфорцелевел](endpointdlp-dlpappenforcelevel.md) , указывающее уровень принудительного применения для соответствующего типа действия DLP конечной точки.

</dd> </dl>





## <a name="remarks"></a>Remarks

Передайте массив этих структур в [длпинитиализинфорцементмоде](endpointdlp-dlpinitializeenforcementmode.md) , чтобы установить режим принудительного применения для набора операций DLP в конечной точке.

## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |


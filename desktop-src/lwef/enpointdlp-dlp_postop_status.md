---
description: Указывает сведения о состоянии операции DLP конечной точки.
title: Структура DLP_POSTOP_STATUS (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495825"
---
# <a name="dlp_postop_status-structure"></a>Структура DLP_POSTOP_STATUS

Указывает сведения о состоянии операции DLP конечной точки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Члены

<dl> <dt>

*Версия* \[ окне\]
</dt> <dd>

Значение типа DWORD, указывающее версию API. Это значение всегда должно быть **DLP_POSTOP_STATUS_V_LATEST**. Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*Оператионсукцесс* \[ окне\]
</dt> <dd>

Логическое значение, указывающее, была ли операция открытия успешной.

</dd> </dl>





## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |

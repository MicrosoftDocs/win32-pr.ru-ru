---
description: Указывает сведения о состоянии операции DLP конечной точки.
title: Структура DLP_POSTOP_STATUS (endpointdlp.h)
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
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610234"
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

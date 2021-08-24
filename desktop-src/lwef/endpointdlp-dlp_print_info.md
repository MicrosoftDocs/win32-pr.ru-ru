---
description: Указывает сведения о документе, связанном с операцией печати в конечной точке.
title: Структура DLP_PRINT_INFO (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e55b3dc22c77d85e15499ea0fb2a6634ece044496637c811ae42e4afd632704e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725824"
---
# <a name="dlp_print_info-structure"></a>Структура DLP_PRINT_INFO

Указывает сведения о документе, связанном с операцией печати в конечной точке.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Члены

<dl> <dt>

*Версия* \[ окне\]
</dt> <dd>

Значение типа DWORD, указывающее версию API. Это значение всегда должно быть **DLP_PRINT_INFO_V_LATEST**. Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)статьи.

</dd> </dl>

<dl> <dt>

*Принтернаме* \[ окне\]
</dt> <dd>

ЛПКВСТР, определяющий принтер назначения.

</dd> </dl>

<dl> <dt>

*JobName* \[ окне\]
</dt> <dd>

ЛПКВСТР, указывающий имя задания печати.

</dd> </dl>

<dl> <dt>

*OutputFilename* \[ окне\]
</dt> <dd>

Объект ЛПКВСТР, указывающий путь к выходному файлу при печати в файл.

</dd> </dl>



## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |


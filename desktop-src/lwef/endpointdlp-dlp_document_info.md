---
description: Указывает сведения о документе, связанном с операцией DLP конечной точки.
title: Структура DLP_DOCUMENT_INFO (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495960"
---
# <a name="dlp_document_info-structure"></a>Структура DLP_DOCUMENT_INFO

Указывает сведения о документе, связанном с операцией DLP конечной точки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Члены

<dl> <dt>

*Версия* \[ окне\]
</dt> <dd>

Значение типа DWORD, указывающее версию API. Это значение всегда должно быть **DLP_DOCUMENT_INFO_V_LATEST**. Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)статьи.

</dd> </dl>

<dl> <dt>

*Персистентфиленаме* \[ окне\]
</dt> <dd>

Объект ЛПКВСТР, указывающий исходный путь к документу.

</dd> </dl>

<dl> <dt>

*Локалфиленаме* \[ окне\]
</dt> <dd>

Объект ЛПКВСТР, указывающий путь к реальному резервному файлу документа.

</dd> </dl>



## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |


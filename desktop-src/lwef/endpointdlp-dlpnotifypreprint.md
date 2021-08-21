---
description: Предоставляет системе сведения о документе до начала операции печати.
title: Функция DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1cf0ef44031677495d9b9bedf990877ee931cae245b217faa4225b334df1b3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479445"
---
# <a name="dlpnotifypreprint-function"></a>Функция Длпнотифипрепринт

Предоставляет системе сведения о документе до начала операции печати.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Документинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о печатаемом документе.

</dd> </dl>

<dl> <dt>

*Принтинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) , содержащую сведения о операции печати.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение void.

## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
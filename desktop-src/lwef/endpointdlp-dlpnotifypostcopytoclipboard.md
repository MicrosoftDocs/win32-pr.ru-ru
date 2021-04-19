---
description: Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.
title: Функция Длпнотифипосткопитоклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b4b1a375d68819fc36f82a530a7fe7a8abe881c0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495899"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a>Функция Длпнотифипосткопитоклипбоард

Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Документинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, из которого было скопировано содержимое.

</dd> </dl>

<dl> <dt>

*Опстатус* \[ окне\]
</dt> <dd>

Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции копирования в буфер обмена.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение void.

## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
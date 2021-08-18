---
description: Предоставляет системе сведения о документе до инициации операции сохранения.
title: Функция DlpNotifyPreSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1dbd565ac7a86e381e1e70facf79a2883182260f82c31a2e8a9a3de4f6da8f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778224"
---
# <a name="dlpnotifypresaveasdocument-function"></a>Функция Длпнотифипресавеасдокумент

Предоставляет системе сведения о документе до инициации операции сохранения.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Документинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, который необходимо сохранить.

</dd> </dl>

<dl> <dt>

*Назначение* \[ окне\]
</dt> <dd>

Объект **лпквстр** , содержащий путь назначения сохраняемого документа.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение void.

## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
---
description: Предоставляет системе сведения о документе при входе в цель перетаскивания.
title: Функция Длпнотифентердроптаржет (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495900"
---
# <a name="dlpnotifyenterdroptarget-function"></a>Функция Длпнотифентердроптаржет

Предоставляет системе сведения о документе при входе в цель перетаскивания.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Документинфо* \[ окне\]
</dt> <dd>

Указатель на структуру [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) , содержащую сведения о документе, связанном с операцией Drop.

</dd> </dl>


## <a name="return-value"></a>Возвращаемое значение

Возвращает значение void.

## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
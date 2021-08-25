---
description: Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.
title: Функция DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888584"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Функция Длпмустпастефромсистемклипбоард

Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если вызов в буфер обмена ОС является обязательным; в противном случае — значение FALSE.

## <a name="remarks"></a>Remarks


## <a name="requirements"></a>Требования



| Требование          |    Значение                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 (10,0; Сборка 17763)           |
| DLL<br/>                      | EndpointDlp.dll |
---
description: Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.
title: Функция Длпмустпастефромсистемклипбоард (ендпоинтдлп. h)
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
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495917"
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
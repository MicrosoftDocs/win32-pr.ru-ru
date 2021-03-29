---
description: Освобождает указанные данные атрибута файла.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Функция Сдбфрифилеаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806916"
---
# <a name="sdbfreefileattributes-function"></a>Функция Сдбфрифилеаттрибутес

Освобождает указанные данные атрибута файла.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфилеаттрибутес* \[ окне\]
</dt> <dd>

Структура [**аттринфо**](attrinfo.md) , возвращаемая функцией [**сдбжетфилеаттрибутес**](sdbgetfileattributes.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 





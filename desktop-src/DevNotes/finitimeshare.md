---
description: Инициализирует общий ресурс IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Функция Финитимешаре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657615"
---
# <a name="finitimeshare-function"></a>Функция Финитимешаре

Инициализирует общий ресурс IME.

## <a name="syntax"></a>Синтаксис


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение true** при успешном выполнении или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Эта функция должна вызываться до вызова любых других функций общего доступа IME.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ендимешаре**](endimeshare.md)
</dt> </dl>

 

 

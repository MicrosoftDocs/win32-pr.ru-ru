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
ms.openlocfilehash: 178b39c67d12473663eb93bc300651341a9c459c19680218fa2c6f7a939c688c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691384"
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

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Эта функция должна вызываться до вызова любых других функций общего доступа IME.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ендимешаре**](endimeshare.md)
</dt> </dl>

 

 

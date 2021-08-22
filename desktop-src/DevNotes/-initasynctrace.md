---
description: Инициализирует трассировку.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Функция Инитасинктраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: d64fcf9f787587165c12e675d79cfca641b0ab5086a5cce6b13029da46def974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956303"
---
# <a name="initasynctrace-function"></a>Функция Инитасинктраце

Инициализирует трассировку.

## <a name="syntax"></a>Синтаксис


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 

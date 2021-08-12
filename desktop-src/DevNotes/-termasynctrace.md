---
description: Завершает трассировку.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: Функция Термасинктраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 6857e8e6164392a12604779d51914d7d297ec89a3890adec000cf662019a7485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668803"
---
# <a name="termasynctrace-function"></a>Функция Термасинктраце

Завершает трассировку.

## <a name="syntax"></a>Синтаксис


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 

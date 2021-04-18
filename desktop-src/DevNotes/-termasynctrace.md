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
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648985"
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

## <a name="remarks"></a>Комментарии

Exstrace.dll является необязательным компонентом, который устанавливается с протоколом SMTP и протоколом NNTP.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 

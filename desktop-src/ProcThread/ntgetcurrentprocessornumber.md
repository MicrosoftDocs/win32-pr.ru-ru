---
description: Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Функция Нтжеткуррентпроцессорнумбер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: f45ee39e9599e2d77d77131eb64c2a9037de1f4ba31f907ac5c9ea562a706c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032194"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Функция Нтжеткуррентпроцессорнумбер

\[**Нтжеткуррентпроцессорнумбер** может быть изменен или недоступен в будущих версиях Windows. Вместо этого приложения должны использовать функцию [**жеткуррентпроцессорнумбер**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]

Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.

## <a name="syntax"></a>Синтаксис


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает текущий номер процессора.

## <a name="remarks"></a>Remarks

Эта функция используется для предоставления сведений для оценки производительности процесса.

Эта функция не имеет связанной библиотеки импорта. Для динамической привязки к Ntdll.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Несколько процессоров](multiple-processors.md)
</dt> <dt>

[Функции процессов и потоков](process-and-thread-functions.md)
</dt> <dt>

[Процессы](child-processes.md)
</dt> </dl>

 

 

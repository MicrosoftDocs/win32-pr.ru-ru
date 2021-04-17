---
description: Возвращает текущее значение счетчика производительности и, при необходимости, частоту счетчика производительности.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Функция Нткуериперформанцекаунтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665365"
---
# <a name="ntqueryperformancecounter-function"></a>Функция Нткуериперформанцекаунтер

\[Эта функция не поддерживается и не должна использоваться. Вместо этого используйте функции **QueryPerformanceCounter** и **куериперформанцефрекуенци** .\]

Возвращает текущее значение счетчика производительности и, при необходимости, частоту счетчика производительности.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PerformanceCounter* \[ заполняет\]
</dt> <dd>

Адрес переменной, получающей текущее значение счетчика производительности.

</dd> <dt>

*PerformanceFrequency* \[ out, необязательно\]
</dt> <dd>

Адрес переменной для получения частоты счетчика производительности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, она возвращает код **NTSTATUS** **\_ Success**, в противном случае возвращается код ошибки, например **\_ \_ нарушение прав доступа к состоянию**.

## <a name="remarks"></a>Комментарии

Нет файла заголовка, доступного для **нткуериперформанцекаунтер**. Следует использовать альтернативные функции, указанные выше, хотя функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) можно использовать для динамической привязки к Ntdll.dll.

Частота производительности — это частота счетчика производительности в герцах, особенно в количестве в секунду. Это значение зависит от реализации. Если в реализации отсутствует оборудование для поддержки времени производительности, возвращается значение 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 

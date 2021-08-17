---
UID: ''
title: Функция Каптурестаккбакктраце
description: Захватывает обратную трассировку стека, выполнив проход вверх по стеку.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0b6cad22d7a52908c3aa02bef7e23a57899e421f87bda00660519750de742919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279506"
---
# <a name="capturestackbacktrace-function"></a>Функция Каптурестаккбакктраце

## <a name="description"></a>Описание

Фиксирует обратную трассировку стека, выполнив проход вверх по стеку и записывая сведения для каждого кадра.

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a>Параметры

### <a name="framestoskip-in"></a>Фраместоскип [in]

Число кадров, которые нужно пропустить с начала обратной трассировки.

### <a name="framestocapture-in"></a>Фраместокаптуре [in]

Число кадров для записи.
Вы можете захватить до **максушорт** кадров.

**Windows Server 2003 и Windows XP:**  Сумма параметров *фраместоскип* и *фраместокаптуре* должна быть меньше 63.

### <a name="backtrace-out"></a>Невыполненная трассировка [out]

Массив указателей, захваченных из текущей трассировки стека.

### <a name="backtracehash-out-optional"></a>Бакктрацехаш [out, необязательно]

Значение, которое может быть использовано для Организации хэш-таблиц.
Если этот параметр имеет **значение NULL**, хэш-значение не вычислено.

Это значение вычисляется на основе значений указателей, возвращаемых в массиве отслеживаний.
Две идентичные трассировки стека будут формировать идентичные хэш-значения.

## <a name="returns"></a>Возвращаемое значение

Число захваченных кадров.

## <a name="remarks"></a>Remarks

функция **каптурестаккбакктраце** определяется как функция **ртлкаптурестаккбакктраце** (определение включается в Windows SDK, начиная с Windows Vista).
Дополнительные сведения см. в разделе Винбасе. h и WinNT. h.

## <a name="see-also"></a>См. также раздел

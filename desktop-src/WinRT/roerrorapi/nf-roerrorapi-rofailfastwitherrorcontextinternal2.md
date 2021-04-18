---
title: Функция RoFailFastWithErrorContextInternal2
description: Вызывает исключение, которое не является непрерывным в текущем процессе, а также позволяет включить дополнительный контекст ошибки, еще не записанный операционной системой.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "105719160"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>Функция RoFailFastWithErrorContextInternal2

Вызывает исключение, которое не является непрерывным в текущем процессе, а также позволяет включить дополнительный контекст ошибки, который еще не был захвачен операционной системой (ОС).

## <a name="syntax"></a>Синтаксис

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Параметры

`hrError`

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Значение **HRESULT** , связанное с текущей ошибкой. Исключение вызывается для любого значения *хреррор*.

`cStowedExceptions`

Тип: **[ulong](../../winprog/windows-data-types.md)**

Число элементов в массиве *астоведексцептионпоинтерс* .

`aStowedExceptionPointers`

Тип: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Массив указателей на [**STOWED_EXCEPTION_INFORMATION_V2ные**](../../wer/stowed-exception-information-v2.md) структуры. Каждая структура содержит сведения, описывающие исключение заполнения. Сведения в этих структурах затем отправляются в отчеты об ошибках Windows (WER) вместе со сведениями об исключении заполнения, которые были перехвачены платформой.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

**RoFailFastWithErrorContextInternal2** не связан с библиотекой импорта или файлом заголовка. Его можно вызвать, сначала используя функцию [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (для загрузки `ComBase.dll` ), а затем вызвав функцию [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса **RoFailFastWithErrorContextInternal2**.

Дополнительные сведения см. в разделе [функция рофаилфаствисеррорконтекст](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | Н/Д |
| **Библиотека** | Н/Д |
| **КОМПОНОВКИ** | ComBase.dll |

## <a name="see-also"></a>См. также раздел

* [Функция Рофаилфаствисеррорконтекст](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)
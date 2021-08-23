---
description: Возвращает размер и расположение динамически выгруженного списка модулей для текущего процесса.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Функция Ртлжетунлоадевенттрацеекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 35c4001851cc12701152f983c51a800d8f1846e015f5cf4d967c6371d9807578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571364"
---
# <a name="rtlgetunloadeventtraceex-function"></a>Функция Ртлжетунлоадевенттрацеекс

Возвращает размер и расположение динамически выгруженного списка модулей для текущего процесса.

## <a name="syntax"></a>Синтаксис


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ElementSize* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая содержит размер элемента в списке.

</dd> <dt>

*ElementCount* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая содержит число элементов в списке.

</dd> <dt>

*Евенттраце* \[ заполняет\]
</dt> <dd>

Указатель на массив структур **\_ \_ \_ трассировки событий "справа налево" выгрузки** . Дополнительные сведения см. в подразделе "Примечания".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Загрузчик хранит выгруженные сведения о событиях в расположениях, которые могут быть прочитаны между процессами, используя преимущества того факта, что Ntdll.dll загружается по одному и тому же базовому адресу во всех процессах. Если отладчику требуется запросить выгруженную информацию о модулях, он вызывает эту функцию для определения адреса, в котором находятся переменные, а затем запрашивает виртуальную память в целевом процессе по этим адресам для чтения фактических значений.

Каждый элемент в списке определяется следующим образом.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

Эта функция не имеет связанного файла заголовка. связанная библиотека импорта, Ntdll. lib, доступна в наборе драйверов Windows (WDK). Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 

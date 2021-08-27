---
description: Позволяет коду дампа получать выгруженные сведения о модуле из Ntdll.dll для хранения в минидампа.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Функция Ртлжетунлоадевенттраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058594"
---
# <a name="rtlgetunloadeventtrace-function"></a>Функция Ртлжетунлоадевенттраце

\[эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Позволяет коду дампа получать выгруженные сведения о модуле из Ntdll.dll для хранения в минидампа.

## <a name="syntax"></a>Синтаксис


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает указатель на массив. Дополнительные сведения см. в подразделе "Примечания".

## <a name="remarks"></a>Remarks

Массив Ртлпунлоадевенттраце определяется следующим образом:

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

Эта функция не имеет связанного файла заголовка. связанная библиотека импорта, Ntdll. lib, доступна в наборе драйверов Windows (WDK). Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 

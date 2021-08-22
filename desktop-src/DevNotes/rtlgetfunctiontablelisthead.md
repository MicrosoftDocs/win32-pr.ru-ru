---
description: Позволяет отладчику анализировать сведения о таблице динамической функции.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Функция Ртлжетфунктионтаблелиссеад
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666734"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Функция Ртлжетфунктионтаблелиссеад

\[эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Позволяет отладчику анализировать сведения о таблице динамической функции.

## <a name="syntax"></a>Синтаксис


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на заголовок списка таблиц функций.

## <a name="remarks"></a>Remarks

обратите внимание, Windows что для некоторых определений требуется файл заголовка нтдеф. h для набора драйверов (WDK). Связанная библиотека импорта, NTDLL. lib, доступна в WDK. Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 

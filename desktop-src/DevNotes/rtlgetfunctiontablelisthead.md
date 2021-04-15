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
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669032"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Функция Ртлжетфунктионтаблелиссеад

\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Позволяет отладчику анализировать сведения о таблице динамической функции.

## <a name="syntax"></a>Синтаксис


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на заголовок списка таблиц функций.

## <a name="remarks"></a>Комментарии

Обратите внимание, что для некоторых определений требуется файл заголовка Нтдеф. h для комплекта драйверов Windows (WDK). Связанная библиотека импорта, NTDLL. lib, доступна в WDK. Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 

---
description: Очищает кэш базы данных оболочки совместимости. Эту функцию следует вызывать после установки новой базы данных оболочек совместимости.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Функция Шимфлушкаче
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072338"
---
# <a name="shimflushcache-function"></a>Функция Шимфлушкаче

Очищает кэш базы данных оболочки совместимости. Эту функцию следует вызывать после установки новой базы данных оболочек совместимости.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* \[ в необязательное\]
</dt> <dd>

Использующ значение должно быть равно 0.

</dd> <dt>

*HINSTANCE* \[ в необязательное\]
</dt> <dd>

Использующ значение должно быть равно 0.

</dd> <dt>

*лпсзкмдлине* \[ в необязательное\]
</dt> <dd>

Использующ значение должно быть равно 0.

</dd> <dt>

*нкмдшов* \[ окне\]
</dt> <dd>

Использующ значение должно быть равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Комментарии

Вызывающий объект должен быть администратором.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**басефлушаппкомпаткаче**](baseflushappcompatcache.md)
</dt> </dl>

 

 





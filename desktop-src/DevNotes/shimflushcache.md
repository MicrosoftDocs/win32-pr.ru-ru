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
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075918"
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

## <a name="remarks"></a>Remarks

Вызывающий объект должен быть администратором.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**басефлушаппкомпаткаче**](baseflushappcompatcache.md)
</dt> </dl>

 

 





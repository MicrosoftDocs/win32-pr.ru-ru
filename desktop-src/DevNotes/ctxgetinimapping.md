---
description: Определяет, находится ли сервер терминалов в режиме установки (только на сервере терминалов Windows 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Функция Ктксжетинимаппинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648991"
---
# <a name="ctxgetinimapping-function"></a>Функция Ктксжетинимаппинг

\[Эта функция не поддерживается и не должна использоваться. Он может измениться или исчезнуть полностью без предварительного уведомления. Вместо этого используйте **верифиверсионинфо**.\]

Определяет, находится ли сервер терминалов в режиме установки (только на сервере терминалов Windows 4,0).

## <a name="syntax"></a>Синтаксис


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение false** , если сервер терминалов находится в режиме установки, и **значение true** , если он находится в режиме выполнения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**верифиверсионинфо**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 

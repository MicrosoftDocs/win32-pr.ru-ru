---
description: определяет, находится ли сервер терминалов в режиме установки (только на Терминал Windows server 4,0).
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
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654214"
---
# <a name="ctxgetinimapping-function"></a>Функция Ктксжетинимаппинг

\[Эта функция не поддерживается и не должна использоваться. Он может измениться или исчезнуть полностью без предварительного уведомления. Вместо этого используйте **верифиверсионинфо**.\]

определяет, находится ли сервер терминалов в режиме установки (только на Терминал Windows server 4,0).

## <a name="syntax"></a>Синтаксис


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение false** , если сервер терминалов находится в режиме установки, и **значение true** , если он находится в режиме выполнения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**верифиверсионинфо**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 

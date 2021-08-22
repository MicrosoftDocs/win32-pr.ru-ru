---
description: Определяет, находится ли сервер терминалов в режиме установки.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Функция Термсрваппинсталлмоде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f6bf6408fb7bd72b1757b8ca2219e1bbd2cc612829359fdcaf090786e8e7e98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570894"
---
# <a name="termsrvappinstallmode-function"></a>Функция Термсрваппинсталлмоде

\[Эта функция не поддерживается и не должна использоваться. Он может измениться или исчезнуть полностью без предварительного уведомления.\]

Определяет, находится ли сервер терминалов в режиме установки.

## <a name="syntax"></a>Синтаксис


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если сервер терминалов находится в режиме установки, и **значение false** , если он находится в режиме выполнения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 





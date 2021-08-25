---
description: Возвращает путь к модулю.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: Функция _GetModuleFileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a10ff54d7f118dc71e12cdb5b29e28d3b3dd6e60c7b51c263af8c62c1264968c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911924"
---
# <a name="_getmodulefilename-function"></a>\_Функция GetModuleFileName

\[Эта функция является оболочкой для функции **GetModuleFileName** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать **GetModuleFileName** напрямую.\]

Возвращает путь к модулю. См. [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).

## <a name="syntax"></a>Синтаксис


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 

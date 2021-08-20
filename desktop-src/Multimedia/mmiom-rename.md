---
title: Сообщение MMIOM_RENAME (Ммсистем. h)
description: '\_Сообщение о переименовании ммиом отправляется в процедуру ввода-вывода функцией ммиоренаме, чтобы запросить переименование указанного файла.'
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- сообщение MMIOM_RENAME Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065314"
---
# <a name="mmiom_rename-message"></a>ММИОМ \_ Переименование сообщения

Сообщение **о \_ переименовании ммиом** отправляется в процедуру ввода-вывода функцией [**ммиоренаме**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) , чтобы запросить переименование указанного файла.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*лпсзолдфиленаме*
</dt> <dd>

Указатель на строку, содержащую имя файла для переименования.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*лпсзневфиленаме*
</dt> <dd>

Указатель на строку, содержащую новое имя файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если файл успешно переименован, возвращаемое значение равно нулю. Если указанный файл не найден, возвращается значение ММИОЕРР \_ FILENOTFOUND.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



 


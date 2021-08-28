---
description: Возвращает адрес функции из библиотеки DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: Функция _GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d35d623ff7c7873534bd835c138dba490274e5caddf839fc71765cda59b9f00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053204"
---
# <a name="_getprocaddress_-function"></a>\_\_Функция GetProcAddress

\[Эта функция является оболочкой для функции **GetProcAddress** . Эта функция может быть изменена или недоступна в будущем. Приложения должны вызывать функцию **GetProcAddress** напрямую.\]

Возвращает адрес функции из библиотеки DLL. См. раздел [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).

## <a name="syntax"></a>Синтаксис


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 

---
description: Функция ThunkConnect32 используется 16-разрядными драйверами устройств (для MS-DOS), которые вызывают 32-разрядный ядро.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Функция ThunkConnect32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647965"
---
# <a name="thunkconnect32-function"></a>Функция ThunkConnect32

\[Эта функция поддерживалась для обеспечения обратной совместимости, но отсутствует в текущих версиях Windows. Новые драйверы устройств должны быть 32 или 64-бит и не нуждаются в этой функции.\]

Функция **ThunkConnect32** используется 16-разрядными драйверами устройств (для MS-DOS), которые вызывают 32-разрядный ядро.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*pszDll16* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*pszDll32* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*hInstance* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*Параметр dwReason* 
</dt> <dd>

Не обрабатывается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Всегда возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 





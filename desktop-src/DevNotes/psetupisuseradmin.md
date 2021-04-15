---
description: Указывает, является ли текущий пользователь администратором.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: Функция Псетуписусерадмин
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669015"
---
# <a name="psetupisuseradmin-function"></a>Функция Псетуписусерадмин

\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]

Указывает, является ли текущий пользователь администратором.

## <a name="syntax"></a>Синтаксис


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если текущий пользователь является администратором; в противном случае — **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 

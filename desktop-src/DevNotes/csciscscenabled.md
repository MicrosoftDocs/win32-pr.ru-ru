---
description: Определяет, включена ли автономные файлы.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: Функция КсЦисксценаблед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8678e48aedf6bda6cdb8beb5b78bb310a16d2829ebf6f3e5b0b8525c135aaf03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815464"
---
# <a name="csciscscenabled-function"></a>Функция КсЦисксценаблед

\[Эта функция не поддерживается и не должна использоваться.\]

Определяет, включена ли автономные файлы.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если автономные файлы включена, и **false** в противном случае.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ксккуеридатабасестатус**](cscquerydatabasestatus.md)
</dt> </dl>

 

 

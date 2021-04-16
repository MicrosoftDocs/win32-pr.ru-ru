---
description: Функция Жетдллверсион получает номер версии Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Функция Жетдллверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657130"
---
# <a name="getdllversion-function"></a>Функция Жетдллверсион

\[Эта функция больше не поддерживается, поэтому ее поведение не гарантируется. \]

Функция **жетдллверсион** получает номер версии Cabinet.dll.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Номер версии файла (см. [ресурс versionInfo](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дллжетверсион**](dllgetversion.md)
</dt> </dl>

 

 

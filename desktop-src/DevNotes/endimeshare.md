---
description: Завершает общий ресурс IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Функция Ендимешаре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 079a8719aa8e48e8ae880f2ce2a83d5e4d0f89fda85298ec015a3f77acebeb9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653444"
---
# <a name="endimeshare-function"></a>Функция Ендимешаре

Завершает общий ресурс IME.

## <a name="syntax"></a>Синтаксис


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Эта функция должна вызываться после вызова последней функции общего ресурса IME.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**финитимешаре**](finitimeshare.md)
</dt> </dl>

 

 

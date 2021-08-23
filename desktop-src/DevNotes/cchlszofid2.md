---
description: Декодирует и сохраняет строку.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Функция CchLszOfId2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815474"
---
# <a name="cchlszofid2-function"></a>Функция CchLszOfId2

Декодирует и сохраняет строку.

## <a name="syntax"></a>Синтаксис


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*id* 
</dt> <dd>

Идентификатор строки в файле ресурсов для декодирования и сохранения. Допустимость строки не проверяется.

</dd> <dt>

*лсз* 
</dt> <dd>

Указатель на буфер с длиной *кбмакс*. Строки, длина которых превышает *кбмакс* , усекаются.

</dd> <dt>

*кбмакс* 
</dt> <dd>

Максимальная длина строки, сохраняемой в параметре *лсз* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает декодированную строку.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 

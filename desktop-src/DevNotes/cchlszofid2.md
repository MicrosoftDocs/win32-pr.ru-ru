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
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657785"
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

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 

---
description: Функция Мержеблоб копирует все записи из исходного BLOB-объекта в целевой большой двоичный объект.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Функция Мержеблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5c0ce93235a0c46286b9bfbef0773a5584f3db774aa52991b4e0eaa9dd38352f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677194"
---
# <a name="mergeblob-function"></a>Функция Мержеблоб

Функция **мержеблоб** копирует все записи из исходного BLOB-объекта в целевой большой двоичный объект.

## <a name="syntax"></a>Синтаксис


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдстблоб* \[ в, out\]
</dt> <dd>

Обработайте с целевым BLOB-объектом. На входе этот BLOB-объект содержит исходные сведения. В выходных данных этот большой двоичный объект содержит исходные сведения и все данные исходного большого двоичного объекта.

</dd> <dt>

*хсркблоб* \[ окне\]
</dt> <dd>

Обработайте с исходным BLOB-объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="remarks"></a>Remarks

Записи, общие для исходного и целевого файлов, будут перезаписаны данными из исходного большого двоичного объекта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 





---
description: Функция Регкреатеблобкэй сохраняет большой двоичный объект в заданном разделе реестра.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Функция Регкреатеблобкэй (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889654"
---
# <a name="regcreateblobkey-function"></a>Функция Регкреатеблобкэй

Функция **регкреатеблобкэй** сохраняет большой двоичный объект в заданном разделе реестра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*hKey* \[ заполняет\]
</dt> <dd>

Обработайте с разделом реестра, в котором будет храниться большой двоичный объект.

</dd> <dt>

*сзблобнаме* \[ окне\]
</dt> <dd>

Имя (определяется приложением), представляющее большой двоичный объект в реестре.

</dd> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик сохраняемого большого двоичного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[регопенблобкэй](regopenblobkey.md)
</dt> </dl>

 

 





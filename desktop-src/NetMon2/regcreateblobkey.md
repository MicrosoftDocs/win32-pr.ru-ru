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
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674420"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[регопенблобкэй](regopenblobkey.md)
</dt> </dl>

 

 





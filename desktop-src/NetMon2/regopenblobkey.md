---
description: Функция Регопенблобкэй извлекает большой двоичный объект, хранящийся в указанном разделе реестра.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Функция Регопенблобкэй (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674419"
---
# <a name="regopenblobkey-function"></a>Функция Регопенблобкэй

Функция **регопенблобкэй** извлекает большой двоичный объект, хранящийся в указанном разделе реестра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*hKey* \[ окне\]
</dt> <dd>

Обработайте с ключом реестра, содержащим большой двоичный объект.

</dd> <dt>

*сзблобнаме* \[ окне\]
</dt> <dd>

Имя, идентифицирующее данный большой двоичный объект в реестре.

</dd> <dt>

*фблоб* \[ заполняет\]
</dt> <dd>

Указатель на возвращаемый большой двоичный объект.

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

[регкреатеблобкэй](regcreateblobkey.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 5d372d6cc69c4e80691f96075aaa0d9030c90d06fc8256f85a7ed2dc894f3fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364153"
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

 

 





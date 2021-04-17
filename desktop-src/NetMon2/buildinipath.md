---
description: Функция Буилдинипас возвращает полный путь к INI-файлу, который соответствует введенным данным.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Функция Буилдинипас (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663649"
---
# <a name="buildinipath-function"></a>Функция Буилдинипас

Функция **буилдинипас** возвращает полный путь к INI-файлу, который соответствует введенным данным.

## <a name="syntax"></a>Синтаксис


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*FullPath* 
</dt> <dd>

Буфер, который получает полное имя INI-файла.

</dd> <dt>

*инифиленаме* 
</dt> <dd>

Имя INI-файла (полное имя файла минус расширение имени файла).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на полное имя INI-файла.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

Путь, возвращаемый этой функцией, является полным путем к INI-файлу, который соответствует введенным данным. Например, если ввести КСНС или TCP, функция создает путь к Xns.ini или Tcp.ini соответственно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





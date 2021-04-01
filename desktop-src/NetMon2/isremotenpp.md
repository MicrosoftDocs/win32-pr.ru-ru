---
description: Функция Исремотенпп указывает, указывает ли заданный большой двоичный объект удаленный НПП.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Функция Исремотенпп (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812694"
---
# <a name="isremotenpp-function"></a>Функция Исремотенпп

Функция **исремотенпп** указывает, указывает ли заданный большой двоичный объект удаленный НПП.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение **true**.

## <a name="remarks"></a>Комментарии

Используйте эту функцию, чтобы проверить, существует ли удаленная Категория.

Убедитесь, что имена удаленного и локального компьютеров отличаются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 





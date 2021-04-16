---
description: Функция Дестройблоб освобождает всю память, связанную с большим двоичным объектом, а затем уничтожает большой двоичный объект.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Функция Дестройблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664416"
---
# <a name="destroyblob-function"></a>Функция Дестройблоб

Функция **дестройблоб** освобождает всю память, связанную с большим двоичным объектом, а затем уничтожает большой двоичный объект.

## <a name="syntax"></a>Синтаксис


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для объекта, который уничтожается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.

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

[CreateBlob](createblob.md)
</dt> </dl>

 

 





---
description: Функция Дупликатеблоб копирует конкретный большой двоичный объект.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Функция Дупликатеблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650997"
---
# <a name="duplicateblob-function"></a>Функция Дупликатеблоб

Функция **дупликатеблоб** копирует конкретный большой двоичный объект.

## <a name="syntax"></a>Синтаксис


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсркблоб* \[ окне\]
</dt> <dd>

Обработчик для копируемого большого двоичного объекта.

</dd> <dt>

*хблобсатвиллбекреатед* \[ заполняет\]
</dt> <dd>

Обработчик для повторяющегося большого двоичного объекта.

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
</dt> <dt>

[дестройблоб](destroyblob.md)
</dt> </dl>

 

 





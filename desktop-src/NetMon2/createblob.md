---
description: Функция CreateBlob создает пустой большой двоичный объект.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Функция CreateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 1c5a74a2008993aba40b97e6fce779398132dbeae0428d4c7ae2054640a4159a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744714"
---
# <a name="createblob-function"></a>Функция CreateBlob

Функция **CreateBlob** создает пустой большой двоичный объект.

## <a name="syntax"></a>Синтаксис


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фблоб* \[ заполняет\]
</dt> <dd>

Указатель на переменную, в которой возвращается указатель на новый большой двоичный объект.

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

[дестройблоб](destroyblob.md)
</dt> </dl>

 

 





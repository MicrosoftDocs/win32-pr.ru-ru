---
description: Функция Жеткаптуретоталфрамес возвращает общее число кадров в записи.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Функция Жеткаптуретоталфрамес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896782"
---
# <a name="getcapturetotalframes-function"></a>Функция Жеткаптуретоталфрамес

Функция **жеткаптуретоталфрамес** возвращает общее число кадров в записи.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкаптуре* \[ окне\]
</dt> <dd>

Обработчик для записи. Дополнительные сведения о получении маркера записи см. в подразделе "Примечания" этой статьи **жеткаптуретоталфрамес** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение — это общее число кадров в записи.

Если функция завершается неудачно, возвращается значение 0.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жеткаптуретоталфрамес** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





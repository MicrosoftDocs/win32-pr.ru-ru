---
description: Функция Финдпропертинстанце находит первый экземпляр свойства, указанного параметром Хпроперти.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Функция Финдпропертинстанце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662195"
---
# <a name="findpropertyinstance-function"></a>Функция Финдпропертинстанце

Функция **финдпропертинстанце** находит первый экземпляр свойства, указанного параметром *хпроперти* .

## <a name="syntax"></a>Синтаксис


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма. Маркер кадра можно извлечь с помощью вызова функции [noframes](getframe.md) .

</dd> <dt>

*хпроперти* \[ окне\]
</dt> <dd>

Обработчик для свойства, которое необходимо найти. Маркер свойства может быть получен путем вызова функции- [Свойства](getproperty.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно (то есть, если свойство найдено), возвращаемое значение является указателем на первый экземпляр свойства.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

Чтобы получить следующий экземпляр свойства, вызовите [финдпропертинстанцерестарт](findpropertyinstancerestart.md).

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md)могут вызывать функцию **финдпропертинстанце** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[финдпропертинстанцерестарт](findpropertyinstancerestart.md)
</dt> </dl>

 

 





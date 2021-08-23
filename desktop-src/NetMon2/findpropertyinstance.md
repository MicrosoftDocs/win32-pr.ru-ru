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
ms.openlocfilehash: ac8b7d34b33bb76bfffc26b3ae6fc455857fafb65a9a2aef7e91fd0c2763adc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938585"
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

## <a name="remarks"></a>Remarks

Чтобы получить следующий экземпляр свойства, вызовите [финдпропертинстанцерестарт](findpropertyinstancerestart.md).

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md)могут вызывать функцию **финдпропертинстанце** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[финдпропертинстанцерестарт](findpropertyinstancerestart.md)
</dt> </dl>

 

 





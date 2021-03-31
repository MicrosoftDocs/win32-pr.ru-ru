---
description: Функция-свойство возвращает маркер для заданного свойства.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Функция Property (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990898"
---
# <a name="getproperty-function"></a>Функция Property

Функция- **свойство** возвращает маркер для заданного свойства.

## <a name="syntax"></a>Синтаксис


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпротокол* \[ окне\]
</dt> <dd>

Обработчик для протокола.

</dd> <dt>

*PropertyName* \[ окне\]
</dt> <dd>

Имя свойства (например, **CHECKSUM**).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является маркером свойства.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

Функцию **Property** можно использовать для получения маркера свойства, необходимого для размещения экземпляров свойства. Функции, используемые для размещения экземпляров свойств, — это [финдпропертинстанце](findpropertyinstance.md) (который находит первый экземпляр) и [финдпропертинстанцерестарт](findpropertyinstancerestart.md) (который находит следующий экземпляр).

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **Property** .

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

[финдпропертинстанце](findpropertyinstance.md)
</dt> <dt>

[финдпропертинстанцерестарт](findpropertyinstancerestart.md)
</dt> </dl>

 

 





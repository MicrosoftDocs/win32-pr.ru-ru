---
description: Функция Дестройпротокол уничтожает протокол, создаваемый функцией Креатепротокол.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Функция Дестройпротокол (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c3a89bfd74a01a7455ecd9393d913ddd906474ceabd1c8884f187444cb483a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911144"
---
# <a name="destroyprotocol-function"></a>Функция Дестройпротокол

Функция **дестройпротокол** уничтожает протокол, создаваемый функцией **креатепротокол** .

## <a name="syntax"></a>Синтаксис


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпротокол* \[ окне\]
</dt> <dd>

Обработчик для уничтожения протокола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет.

## <a name="remarks"></a>Remarks

Библиотека DLL анализатора вызывает функцию **дестройпротокол** во время реализации [DllMain](dllmain-parser.md). **Дестройпротокол** вызывается, когда операционная система собирается выгрузить библиотеку DLL.



| Для получения информации о                                        | См.                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Какие анализаторы и как они работают с сетевой монитор. | [Средства синтаксического анализа](parsers.md)                                  |
| Реализация функции **DllMain** включает пример.         | [Реализация DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 





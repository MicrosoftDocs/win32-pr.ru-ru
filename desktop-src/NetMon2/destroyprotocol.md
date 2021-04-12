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
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264367"
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
| Какие анализаторы и как они работают с сетевой монитор. | [Анализаторы](parsers.md)                                  |
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

 

 





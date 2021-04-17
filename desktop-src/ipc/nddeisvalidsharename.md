---
description: Определяет, использует ли имя общего ресурса правильный синтаксис.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Функция Нддеисвалидшаренаме (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682434"
---
# <a name="nddeisvalidsharename-function"></a>Функция Нддеисвалидшаренаме

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]

Определяет, использует ли имя общего ресурса правильный синтаксис.

## <a name="syntax"></a>Синтаксис


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя_общего_ресурса* \[ окне\]
</dt> <dd>

Имя общей папки для проверки. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если имя общего ресурса имеет допустимый синтаксис, то возвращаемое значение не равно нулю.

Если имя общего ресурса не имеет допустимого синтаксиса, возвращаемое значение равно нулю.

## <a name="remarks"></a>Комментарии

Эта функция также вызывается [**нддешареадд**](nddeshareadd.md) при создании общего ресурса DDE.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Нддеапи. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нддеапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Нддеисвалидшаренамев** (Юникод) и **нддеисвалидшаренамеа** (ANSI)<br/>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о сетевом платформа динамических данных Exchange](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> <dt>

[**нддешареадд**](nddeshareadd.md)
</dt> </dl>

 

 





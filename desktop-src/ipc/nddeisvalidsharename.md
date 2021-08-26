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
ms.openlocfilehash: 3e289429047d8d1cee4f525a9f45a9abe1dd8eb51bcf57e83e39876fba9a5a89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964004"
---
# <a name="nddeisvalidsharename-function"></a>Функция Нддеисвалидшаренаме

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают ндде \_ не \_ реализованы.\]

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

## <a name="remarks"></a>Remarks

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

[общие сведения о Exchange сетевых платформа динамических данных](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> <dt>

[**нддешареадд**](nddeshareadd.md)
</dt> </dl>

 

 





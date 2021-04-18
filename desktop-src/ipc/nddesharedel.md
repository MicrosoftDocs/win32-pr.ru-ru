---
description: Удаляет общую папку DDE из диспетчера общей базы данных DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Функция Нддешаредел (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682433"
---
# <a name="nddesharedel-function"></a>Функция Нддешаредел

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]

Удаляет общую папку DDE из диспетчера общей базы данных DDE (DSDM).

## <a name="syntax"></a>Синтаксис


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзсервер* \[ окне\]
</dt> <dd>

Имя сервера, DSDM которого необходимо изменить.

</dd> <dt>

*лпсзшаренаме* \[ окне\]
</dt> <dd>

Имя общего ресурса, удаляемого из DSDM. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*вресервед* \[ окне\]
</dt> <dd>

Зарезервировано. Этот параметр должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.

Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).

## <a name="remarks"></a>Комментарии

Чтобы удалить общий ресурс DDE из DSDM, необходимо иметь соответствующие права доступа. Автор общего ресурса имеет право на удаление.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Нддеапи. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нддеапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Нддешаределв** (Юникод) и **нддешаредела** (ANSI)<br/>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о сетевом платформа динамических данных Exchange](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> </dl>

 

 





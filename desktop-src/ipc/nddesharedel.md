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
ms.openlocfilehash: 0efd5bb41712e8bee2ee7a5e789d1b006a490c932b48386de27f56a8b1150f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611104"
---
# <a name="nddesharedel-function"></a>Функция Нддешаредел

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают ндде \_ не \_ реализованы.\]

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

## <a name="remarks"></a>Remarks

Чтобы удалить общий ресурс DDE из DSDM, необходимо иметь соответствующие права доступа. Автор общего ресурса имеет право на удаление.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Нддеапи. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нддеапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Нддешаределв** (Юникод) и **нддешаредела** (ANSI)<br/>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[общие сведения о Exchange сетевых платформа динамических данных](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> </dl>

 

 





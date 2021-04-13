---
description: Функция Жетпропертитекст возвращает указатель на текст свойства.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Функция Жетпропертитекст (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342752"
---
# <a name="getpropertytext-function"></a>Функция Жетпропертитекст

Функция **жетпропертитекст** возвращает указатель на текст свойства.

## <a name="syntax"></a>Синтаксис


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфраме* \[ окне\]
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

*лппи* \[ окне\]
</dt> <dd>

Указатель на экземпляр свойства.

</dd> <dt>

*сзбуффер* \[ окне\]
</dt> <dd>

Указатель на текстовую строку свойства.

</dd> <dt>

*BufferSize* \[ окне\]
</dt> <dd>

Размер буфера текстовой строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращаемое значение является указателем на текст свойства.

Если функция завершилась неудачно, возвращается значение **null**.

## <a name="remarks"></a>Комментарии

[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпропертитекст** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Библиотека<br/>                  | <dl> <dt>Нмапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





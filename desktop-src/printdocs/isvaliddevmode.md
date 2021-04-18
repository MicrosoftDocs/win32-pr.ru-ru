---
description: Функция Исвалиддевмоде проверяет допустимость содержимого структуры DEVMODE.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Функция Исвалиддевмоде (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719707"
---
# <a name="isvaliddevmode-function"></a>Функция Исвалиддевмоде

Функция **исвалиддевмоде** проверяет допустимость содержимого структуры DEVMODE.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевмоде* \[ окне\]
</dt> <dd>

Указатель на [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) для проверки.

</dd> <dt>

*девмодесизе* 
</dt> <dd>

Размер входного буфера байтов в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true**, если [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) имеет структурную допустимую структуру. Если обнаружены незначительные ошибки, функция исправит их и возвратит **значение true**.

**Значение false**, если [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) имеет одну или несколько серьезных проблем с структурой. Например, элемент **дмсизе** имеет неправильное соответствие или указывает буфер, который слишком мал. Кроме того, **значение false** , если **Пдевмоде** имеет **значение NULL**.

## <a name="remarks"></a>Комментарии

Не проверяются поля частного драйвера принтера [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , а только открытые поля.

Вызывающие объекты должны использовать **дмсизе** + **дмдриверекстра** для **девмодесизе** , только если они гарантируют, что размер входного буфера по крайней мере такой большой. Так как [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) является обычно ненадежными данными, значения, которые находятся во входном буфере на смещениях **дмсизе** и **дмдриверекстра** , также не являются доверенными.

Эта функция является исполняемым в контексте Least-Privileged учетной записи пользователя (LUA).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Винспул. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Винспул. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Винспул. drv</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Исвалиддевмодев** (Юникод) и **исвалиддевмодеа** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 





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
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100532"
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

## <a name="remarks"></a>Remarks

Не проверяются поля частного драйвера принтера [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , а только открытые поля.

Вызывающие объекты должны использовать **дмсизе** + **дмдриверекстра** для **девмодесизе** , только если они гарантируют, что размер входного буфера по крайней мере такой большой. Так как [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) является обычно ненадежными данными, значения, которые находятся во входном буфере на смещениях **дмсизе** и **дмдриверекстра** , также не являются доверенными.

Эта функция является исполняемым в контексте Least-Privileged учетной записи пользователя (LUA).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
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

 

 





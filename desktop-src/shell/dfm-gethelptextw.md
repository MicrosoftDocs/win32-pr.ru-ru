---
description: DFM_GETHELPTEXTW сообщение — позволяет объекту обратного вызова указать строку текста справки.
title: Сообщение DFM_GETHELPTEXTW (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097042"
---
# <a name="dfm_gethelptextw-message"></a>\_Сообщение DFM жеселптекств

Позволяет объекту обратного вызова указать строку текста справки.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идкмд \_ кчмакс* \[ в\]
</dt> <dd>

Слово с низким приоритетом для этого параметра содержит идентификатор команды. Слово в высоком порядке содержит количество символов в буфере *псзтекст* .

</dd> <dt>

*псзтекст* \[ заполняет\]
</dt> <dd>

Строка в Юникоде, заканчивающаяся нулем и содержащая текст справки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию. Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **DFM \_ ЖЕСЕЛПТЕКСТВ** (Юникод)<br/>                                          |



 

 





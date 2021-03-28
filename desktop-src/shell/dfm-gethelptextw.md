---
description: Позволяет объекту обратного вызова указать строку текста справки.
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
ms.openlocfilehash: 7ac1e41046b2d757df96e9acf5722710ae832bf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984308"
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

## <a name="remarks"></a>Примечания

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию. Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **DFM \_ ЖЕСЕЛПТЕКСТВ** (Юникод)<br/>                                          |



 

 





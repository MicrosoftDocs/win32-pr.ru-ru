---
description: DFM_GETHELPTEXT сообщение — позволяет объекту обратного вызова указать строку текста справки.
title: Сообщение DFM_GETHELPTEXT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d1035ae82a8caf4c9ada5a859663d0d20286b433a9bf527831c29157d8dd6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860939"
---
# <a name="dfm_gethelptext-message"></a>\_Сообщение DFM жеселптекст

Позволяет объекту обратного вызова указать строку текста справки.


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идкмд \_ кчмакс* \[ в\]
</dt> <dd>

Слово с низким приоритетом для этого параметра содержит идентификатор команды. Слово в высоком порядке содержит количество символов в буфере *псзтекст* .

</dd> <dt>

*псзтекст* \[ заполняет\]
</dt> <dd>

Строка ANSI, заканчивающаяся нулем и содержащая текст справки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию. Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **DFM \_ ЖЕСЕЛПТЕКСТ** (ANSI)<br/>                                              |



 

 





---
description: Уведомляет Ишеллвиев, когда один из его объектов помещается в буфер обмена в результате выполнения команды меню. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_SETCLIPBOARD (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997946"
---
# <a name="sfvm_setclipboard-message"></a>\_Сообщение сфвм сетклипбоард

Уведомляет [**ишеллвиев**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , когда один из его объектов помещается в буфер обмена в результате выполнения команды меню. Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двеффект* \[ окне\]
</dt> <dd>

Use (WPARAM)-2, если элемент вырезан в буфер обмена или (WPARAM)-3, если элемент копируется в буфер обмена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 





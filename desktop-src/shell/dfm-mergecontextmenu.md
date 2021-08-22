---
description: Разрешает обратный вызов для добавления элементов в меню.
title: Сообщение DFM_MERGECONTEXTMENU (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455974"
---
# <a name="dfm_mergecontextmenu-message"></a>\_Сообщение DFM мержеконтекстмену

Разрешает обратный вызов для добавления элементов в меню.


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пккминфо* \[ окне\]
</dt> <dd>

Указатель на структуру [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащую сведения, используемые при слиянии.

</dd> <dt>

*уфлагс* \[ окне\]
</dt> <dd>

Флаги, указывающие, как можно изменить контекстное меню. Этот параметр использует значения КМФ, \_ \* описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Remarks

Если элементы добавляются в контекстное меню, они должны поддерживаться с подпрограммыми, которые отвечают соответствующим образом, когда один из этих элементов вызывается с помощью [**DFM \_ инвокекомманд**](dfm-invokecommand.md).

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от реализации объекта контекстного меню по умолчанию. Существует два интерфейса API для реализации, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 





---
description: Разрешает обратный вызов для добавления элементов в нижнюю часть расширенного меню.
title: Сообщение DFM_MERGECONTEXTMENU_BOTTOM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984301"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>\_Сообщение DFM мержеконтекстмену \_ Bottom

Разрешает обратный вызов для добавления элементов в нижнюю часть расширенного меню.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

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

## <a name="remarks"></a>Примечания

Если элементы добавляются в расширенное контекстное меню, они должны поддерживаться с подпрограммыми, которые отвечают соответствующим образом, когда один из этих элементов вызывается с помощью [**DFM \_ инвокекомманд**](dfm-invokecommand.md).

Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию. Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова. Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 





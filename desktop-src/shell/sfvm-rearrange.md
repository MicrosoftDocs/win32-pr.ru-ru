---
description: Уведомляет Ишеллвиев о необходимости переупорядочения элементов. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_REARRANGE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 03bb5b8d39a85d8ce4fb6e76b75967a642361f502ce3bcb20ca49f276a5221de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941984"
---
# <a name="sfvm_rearrange-message"></a>СФВМ \_ изменить расположение сообщения

Уведомляет [**ишеллвиев**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) о необходимости переупорядочения элементов. Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* \[ окне\]
</dt> <dd>

Передается в [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids). Дополнительные сведения об этом параметре см. в разделе [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .

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



 

 





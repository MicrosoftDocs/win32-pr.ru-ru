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
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081544"
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



 

 





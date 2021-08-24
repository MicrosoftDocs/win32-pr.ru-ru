---
title: Сообщение LVM_GETTILEINFO (Коммктрл. h)
description: Извлекает сведения о плитке в элементе управления "представление списка".
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- элементы управления Windows сообщений LVM_GETTILEINFO
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8141b3a39c47966348dfd823b557c1b0af4cca84a90ba979a358d6ac0eaa4757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079038"
---
# <a name="lvm_gettileinfo-message"></a>\_Сообщение LVM жеттилеинфо

Извлекает сведения о плитке в элементе управления "представление списка".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**лвтилеинфо**</a> , которая получает извлеченные сведения.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Remarks

Мозаичное представление — это новый способ упорядочения и отображения элементов в элементе управления "представление списка". К другим представлениям относятся значок, маленький значок, сведения и список.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






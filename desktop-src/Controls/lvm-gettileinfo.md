---
title: Сообщение LVM_GETTILEINFO (Коммктрл. h)
description: Извлекает сведения о плитке в элементе управления "представление списка".
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Элементы управления Windows для LVM_GETTILEINFO сообщений
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
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071903"
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

## <a name="remarks"></a>Комментарии

Мозаичное представление — это новый способ упорядочения и отображения элементов в элементе управления "представление списка". К другим представлениям относятся значок, маленький значок, сведения и список.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






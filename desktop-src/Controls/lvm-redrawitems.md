---
title: Сообщение LVM_REDRAWITEMS (Коммктрл. h)
description: Заставляет элемент управления "представление списка" перерисовывать диапазон элементов. Это сообщение можно отправить явно или с помощью \_ макроса Редравитемс ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- элементы управления Windows сообщений LVM_REDRAWITEMS
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261734"
---
# <a name="lvm_redrawitems-message"></a>\_Сообщение LVM редравитемс

Заставляет элемент управления "представление списка" перерисовывать диапазон элементов. Это сообщение можно отправить явно или с помощью макроса [**\_ редравитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс первого элемента для перерисовки.

</dd> <dt>

*lParam* 
</dt> <dd>

Индекс последнего элемента для перерисовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Указанные элементы на самом деле не перерисовывается до тех пор, пока окно списка представлений не получит сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) для перерисовки. Для немедленного перерисовки вызовите функцию [**упдатевиндов**](/windows/desktop/api/winuser/nf-winuser-updatewindow) после использования этого макроса.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 


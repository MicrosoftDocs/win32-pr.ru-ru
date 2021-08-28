---
title: Сообщение LB_SETITEMDATA (Winuser. h)
description: Задает значение, связанное с указанным элементом в поле со списком.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- элементы управления Windows сообщений LB_SETITEMDATA
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd9a705014ef770edba5b540a7acbd2512b685d5ebf8ca913df8fa329dc6058a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085334"
---
# <a name="lb_setitemdata-message"></a>Сообщение сетитемдата балансировки нагрузки \_

Задает значение, связанное с указанным элементом в поле со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает отсчитываемый от нуля индекс элемента. Если это значение равно-1, то значение *lParam* применяется ко всем элементам списка.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями. Это означает, что списки не могут содержать более 32 767 элементов. Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.

</dd> <dt>

*lParam* 
</dt> <dd>

Указывает значение, которое должно быть связано с элементом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если возникает ошибка, возвращается значение фунтов \_ Err.

## <a name="remarks"></a>Remarks

Если элемент находится в списке, созданном владельцем, без стиля [**фунта \_ хасстрингс**](list-box-styles.md) , это сообщение заменяет значение, содержащееся в параметре *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**\_ инсертстринг**](lb-insertstring.md) , которое добавляет элемент в список.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ADDSTRING балансировки нагрузки \_**](lb-addstring.md)
</dt> <dt>

[**жетитемдата балансировки нагрузки \_**](lb-getitemdata.md)
</dt> <dt>

[**инсертстринг балансировки нагрузки \_**](lb-insertstring.md)
</dt> </dl>

 

 






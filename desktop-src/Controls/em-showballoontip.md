---
title: Сообщение EM_SHOWBALLOONTIP (Коммктрл. h)
description: В \_ сообщении EM шовбаллунтип отображается всплывающая подсказка, связанная с элементом управления "поле ввода".
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- элементы управления Windows сообщений EM_SHOWBALLOONTIP
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ec2666d18c0f6ce43d5c7644eca0aa2a2cc1f3af72cea03ad34af5ca451cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672327"
---
# <a name="em_showballoontip-message"></a>\_Сообщение ШОВБАЛЛУНТИП EM

В сообщении **EM \_ шовбаллунтип** отображается всплывающая подсказка, связанная с элементом управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**едитбаллунтип**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) , содержащую сведения о всплывающей подсказке для отображения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается с ошибкой, возвращается **значение true**. В противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**едитбаллунтип**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Изменить \_ шовбаллунтип**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 






---
title: Сообщение EM_SHOWBALLOONTIP (Коммктрл. h)
description: В \_ сообщении EM шовбаллунтип отображается всплывающая подсказка, связанная с элементом управления "поле ввода".
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Элементы управления Windows для EM_SHOWBALLOONTIP сообщений
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
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136250"
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

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**едитбаллунтип**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Изменить \_ шовбаллунтип**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 






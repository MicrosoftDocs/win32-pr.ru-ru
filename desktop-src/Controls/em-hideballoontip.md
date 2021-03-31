---
title: Сообщение EM_HIDEBALLOONTIP (Коммктрл. h)
description: Скрывает все всплывающие подсказки, связанные с элементом управления "изменение".
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- Элементы управления Windows для EM_HIDEBALLOONTIP сообщений
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988268"
---
# <a name="em_hideballoontip-message"></a>\_Сообщение ХИДЕБАЛЛУНТИП EM

Скрывает все всплывающие подсказки, связанные с элементом управления "изменение".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

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

[**Изменить \_ хидебаллунтип**](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 






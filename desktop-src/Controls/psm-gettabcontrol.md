---
title: Сообщение PSM_GETTABCONTROL (Пршт. h)
description: Получает маркер для элемента управления вкладки страницы свойств. Это сообщение можно отправить явно или с помощью \_ макроса пропшит.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- элементы управления Windows сообщений PSM_GETTABCONTROL
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e26c9489dc839383552b407a16313c94e1fc3b070d93f1d59ddaf0310134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169664"
---
# <a name="psm_gettabcontrol-message"></a>Сообщение ПСМ в \_ TabControl

Получает маркер для элемента управления вкладки страницы свойств. Это сообщение можно отправить явно или с помощью макроса [**пропшит \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для элемента управления "Вкладка".

## <a name="remarks"></a>Remarks

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 






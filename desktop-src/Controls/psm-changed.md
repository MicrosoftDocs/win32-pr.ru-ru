---
title: Сообщение PSM_CHANGED (Пршт. h)
description: Информирует страницу свойств о том, что информация на странице изменилась. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит Changed.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- элементы управления Windows сообщений PSM_CHANGED
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2002801d21e4e89a6ccf762b9c9932671b210217a950f5494fb736feda35d32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826024"
---
# <a name="psm_changed-message"></a>ПСМ \_ измененное сообщение

Информирует страницу свойств о том, что информация на странице изменилась. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Измененный обработчик на странице.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

На странице свойств будет активирована кнопка **Применить** .

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 






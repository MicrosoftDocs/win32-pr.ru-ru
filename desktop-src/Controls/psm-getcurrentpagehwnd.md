---
title: Сообщение PSM_GETCURRENTPAGEHWND (Пршт. h)
description: Извлекает маркер окна текущей страницы на странице свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит жеткуррентпажехвнд.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- элементы управления Windows сообщений PSM_GETCURRENTPAGEHWND
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0f12c7ed444cf2135fac8d873c1076c04d49f4c9eab8fdb54a962b3885a8cae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985864"
---
# <a name="psm_getcurrentpagehwnd-message"></a>\_Сообщение ПСМ жеткуррентпажехвнд

Извлекает маркер окна текущей страницы на странице свойств. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ жеткуррентпажехвнд**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .

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

Возвращает маркер окна текущей страницы свойств.

## <a name="remarks"></a>Remarks

Используйте сообщение **ПСМ \_ жеткуррентпажехвнд** с немодальными страницами свойств, чтобы определить, когда следует уничтожить диалоговое окно. Когда пользователь нажимает кнопку **ОК** или **Отмена** , **ПСМ \_ жеткуррентпажехвнд** возвращает **значение NULL**, а затем можно использовать функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) для уничтожения диалогового окна.

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 


---
title: Сообщение PSM_GETCURRENTPAGEHWND (Пршт. h)
description: Извлекает маркер окна текущей страницы на странице свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит жеткуррентпажехвнд.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Элементы управления Windows для PSM_GETCURRENTPAGEHWND сообщений
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
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654631"
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

## <a name="remarks"></a>Комментарии

Используйте сообщение **ПСМ \_ жеткуррентпажехвнд** с немодальными страницами свойств, чтобы определить, когда следует уничтожить диалоговое окно. Когда пользователь нажимает кнопку **ОК** или **Отмена** , **ПСМ \_ жеткуррентпажехвнд** возвращает **значение NULL**, а затем можно использовать функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) для уничтожения диалогового окна.

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 


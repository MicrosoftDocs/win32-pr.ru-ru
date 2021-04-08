---
title: Сообщение PSM_ISDIALOGMESSAGE (Пршт. h)
description: Передает сообщение в диалоговое окно страницы свойств и указывает, обрабатывало ли это сообщение диалоговое окно. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит исдиалогмессаже.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Элементы управления Windows для PSM_ISDIALOGMESSAGE сообщений
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892013"
---
# <a name="psm_isdialogmessage-message"></a>\_Сообщение ПСМ исдиалогмессаже

Передает сообщение в диалоговое окно страницы свойств и указывает, обрабатывало ли это сообщение диалоговое окно. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ исдиалогмессаже**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение для проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если сообщение было обработано, или **значение false** , если сообщение не было обработано.

## <a name="remarks"></a>Комментарии

Для передачи сообщений в диалоговое окно страницы свойств в цикле сообщений следует использовать сообщение **ПСМ \_ исдиалогмессаже** с немодальными страницами свойств. В системах, поддерживающих Юникод, для получения сообщений используйте версии [](/windows/desktop/api/winuser/nf-winuser-getmessage) Юникода для функций [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**Жетмессажев** и **пикмессажев**) в Юникоде.

Если возвращаемое значение указывает, что сообщение было обработано, оно не должно передаваться в функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) или [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

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

 


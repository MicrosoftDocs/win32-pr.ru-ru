---
title: Сообщение PSM_ISDIALOGMESSAGE (Пршт. h)
description: Передает сообщение в диалоговое окно страницы свойств и указывает, обрабатывало ли это сообщение диалоговое окно. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит исдиалогмессаже.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- элементы управления Windows сообщений PSM_ISDIALOGMESSAGE
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
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088684"
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

## <a name="remarks"></a>Remarks

Для передачи сообщений в диалоговое окно страницы свойств в цикле сообщений следует использовать сообщение **ПСМ \_ исдиалогмессаже** с немодальными страницами свойств. В системах, поддерживающих Юникод, для получения сообщений используйте версии [](/windows/desktop/api/winuser/nf-winuser-getmessage) Юникода для функций [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**Жетмессажев** и **пикмессажев**) в Юникоде.

Если возвращаемое значение указывает, что сообщение было обработано, оно не должно передаваться в функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) или [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

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

 


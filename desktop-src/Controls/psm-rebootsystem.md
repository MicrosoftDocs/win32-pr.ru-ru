---
title: Сообщение PSM_REBOOTSYSTEM (Пршт. h)
description: Указывает, что необходимо перезапустить систему, чтобы изменения вступили в силу. Сообщение ПСМ ребутсистем можно отправить \_ явным образом или с помощью \_ макроса пропшит ребутсистем.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- элементы управления Windows сообщений PSM_REBOOTSYSTEM
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcfebc931d1dbf01ab053fa2723bdcf361c4be5ef1443b9131115e2300770cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088634"
---
# <a name="psm_rebootsystem-message"></a>\_Сообщение ПСМ ребутсистем

Указывает, что необходимо перезапустить систему, чтобы изменения вступили в силу. Сообщение **ПСМ \_ ребутсистем** можно отправить явным образом или с помощью макроса [**пропшит \_ ребутсистем**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .

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

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Приложение должно отправить это сообщение только в ответ на сообщение [PSN \_ Apply](psn-apply.md) или [PSN \_ киллактиве](psn-killactive.md) Notification.

Это сообщение приводит к тому, что функция [**Страница свойств**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) ВОЗВРАЩАЕТ \_ значение ID псребутсистем, но только в том случае, если пользователь нажмет кнопку **ОК** , чтобы закрыть страницу свойств. Ответственность за перезагрузку системы, которую можно выполнить с помощью функции [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) , несет приложение.

Это сообщение заменяет все сообщения [**ПСМ \_ рестартвиндовс**](psm-restartwindows.md) , которые предшествуют или следуют за ним.

> [!Note]  
> Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 


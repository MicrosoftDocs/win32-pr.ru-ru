---
title: Сообщение PSM_SETCURSELID (Пршт. h)
description: Активирует заданную страницу в таблице свойств на основе идентификатора ресурса страницы. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеткурселбид.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Элементы управления Windows для PSM_SETCURSELID сообщений
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136835"
---
# <a name="psm_setcurselid-message"></a>\_Сообщение ПСМ сеткурселид

Активирует заданную страницу в таблице свойств на основе идентификатора ресурса страницы. Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сеткурселбид**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Идентификатор ресурса страницы для активации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Окно, которое теряет активацию, получает код уведомления [PSN \_ киллактиве](psn-killactive.md) , а окно, получающее активацию, получает код уведомления [PSN \_ сетактиве](psn-setactive.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 






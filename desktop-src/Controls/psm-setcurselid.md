---
title: Сообщение PSM_SETCURSELID (Пршт. h)
description: Активирует заданную страницу в таблице свойств на основе идентификатора ресурса страницы. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеткурселбид.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- элементы управления Windows сообщений PSM_SETCURSELID
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
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877024"
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

## <a name="remarks"></a>Remarks

Окно, которое теряет активацию, получает код уведомления [PSN \_ киллактиве](psn-killactive.md) , а окно, получающее активацию, получает код уведомления [PSN \_ сетактиве](psn-setactive.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 






---
title: Сообщение MCM_SETCURRENTVIEW (Коммктрл. h)
description: Задает текущее представление календаря. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткуррентвиев.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- элементы управления Windows сообщений MCM_SETCURRENTVIEW
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019042"
---
# <a name="mcm_setcurrentview-message"></a>\_Сообщение MCM сеткуррентвиев

Задает текущее представление календаря. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткуррентвиев**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Новое представление. Одна из следующих констант.



| Значение                                                                                                                                                      | Значение                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**МКМВ \_ месяц**</dt> </dl>       | Представление за месяц.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**МКМВ \_ год**</dt> </dl>          | Ежегодное представление.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**МКМВное \_ десятилетие**</dt> </dl>    | Представление десятилетия.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**МКМВ \_ век**</dt> </dl> | Представление "век".<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






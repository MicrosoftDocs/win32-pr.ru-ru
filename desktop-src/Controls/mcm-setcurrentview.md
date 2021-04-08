---
title: Сообщение MCM_SETCURRENTVIEW (Коммктрл. h)
description: Задает текущее представление календаря. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткуррентвиев.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Элементы управления Windows для MCM_SETCURRENTVIEW сообщений
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
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989291"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






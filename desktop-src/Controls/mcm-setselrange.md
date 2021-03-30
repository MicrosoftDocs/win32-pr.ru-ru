---
title: Сообщение MCM_SETSELRANGE (Коммктрл. h)
description: Задает для элемента управления "месячный календарь" определенный диапазон дат. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетселранже.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Элементы управления Windows для MCM_SETSELRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071185"
---
# <a name="mcm_setselrange-message"></a>\_Сообщение MCM сетселранже

Задает для элемента управления "месячный календарь" определенный диапазон дат. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетселранже**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив элементов [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами, содержащий сведения о дате, представляющие ограничения выбора. Первая выбранная дата должна быть указана в *лпсистимеаррай* \[ 0 \] , а последняя выбранная дата должна быть указана в *лпсистимеаррай* \[ 1 \] .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае. Это сообщение не будет выполнено, если применяется к элементу управления "месячный календарь", который не использует многоэлементный стиль [**MCS \_**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Время в элементе управления ' календарь на месяц '](month-calendar-controls.md)
</dt> </dl>

 


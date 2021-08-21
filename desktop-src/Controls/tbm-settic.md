---
title: Сообщение TBM_SETTIC (Коммктрл. h)
description: Задает деление на значение TrackBar в указанной логической позиции.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- элементы управления Windows сообщений TBM_SETTIC
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540024"
---
# <a name="tbm_settic-message"></a>ТБМ \_ Set Message

Задает деление на значение TrackBar в указанной логической позиции.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Расположение деления. Этот параметр может быть любым из целочисленных значений в диапазоне от минимума до максимальной позиции ползунка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если деление имеет значение, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Значение TrackBar создает собственные первый и последний деления. Не используйте это сообщение, чтобы задать первый и последний деления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ жетптикс**](tbm-getptics.md)
</dt> <dt>

[**ТБМ \_ жеттик**](tbm-gettic.md)
</dt> </dl>

 

 






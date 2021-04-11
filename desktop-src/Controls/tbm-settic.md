---
title: Сообщение TBM_SETTIC (Коммктрл. h)
description: Задает деление на значение TrackBar в указанной логической позиции.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Элементы управления Windows для TBM_SETTIC сообщений
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
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135455"
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

## <a name="remarks"></a>Комментарии

Значение TrackBar создает собственные первый и последний деления. Не используйте это сообщение, чтобы задать первый и последний деления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ТБМ \_ жетптикс**](tbm-getptics.md)
</dt> <dt>

[**ТБМ \_ жеттик**](tbm-gettic.md)
</dt> </dl>

 

 






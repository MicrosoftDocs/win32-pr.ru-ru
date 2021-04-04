---
title: Сообщение TB_SETDRAWTEXTFLAGS (Коммктрл. h)
description: Задает флаги рисования текста для панели инструментов.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Элементы управления Windows для TB_SETDRAWTEXTFLAGS сообщений
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989064"
---
# <a name="tb_setdrawtextflags-message"></a>\_Сообщение СЕТДРАВТЕКСТФЛАГС ТБ

Задает флаги рисования текста для панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Один или несколько \_ флагов DT, указанных в [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), которые указывают, какие биты в *lParam* будут использоваться при рисовании текста.

</dd> <dt>

*lParam* 
</dt> <dd>

Один или несколько \_ флагов DT, заданных в [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), которые указывают, как будет нарисован текст кнопки. Это значение будет передано функции **DrawText** при прорисовке текста кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущие флаги рисования текста.

## <a name="remarks"></a>Комментарии

Параметр *wParam* позволяет указать, какие флаги будут использоваться при рисовании текста, даже если эти флаги отключены. Например, если не нужно, \_ чтобы флаг центра DT использовался при рисовании текста, необходимо добавить в \_ *wParam* флаг «центр DT» и не указывать в параметре \_ *lParam* флаг «центр DT». Это предотвращает передачу элементом управления \_ флага центра DT в функцию [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 


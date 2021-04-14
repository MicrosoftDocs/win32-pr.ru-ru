---
title: Сообщение TB_AUTOSIZE (Коммктрл. h)
description: Приводит к изменению размера панели инструментов.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Элементы управления Windows для TB_AUTOSIZE сообщений
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535633"
---
# <a name="tb_autosize-message"></a>Размер \_ сообщения AUTOSIZE для ТБ

Приводит к изменению размера панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение отправляет сообщение **\_ AUTOSIZE** по размеру ТБ после изменения размера панели инструментов либо путем установки размера кнопки или растрового изображения, либо путем добавления строк в первый раз.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






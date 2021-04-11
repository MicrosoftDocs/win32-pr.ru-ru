---
title: Сообщение TB_COMMANDTOINDEX (Коммктрл. h)
description: Возвращает отсчитываемый от нуля индекс для кнопки, связанной с указанным идентификатором команды.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- Элементы управления Windows для TB_COMMANDTOINDEX сообщений
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137850"
---
# <a name="tb_commandtoindex-message"></a>\_Сообщение КОММАНДТОИНДЕКС ТБ

Возвращает отсчитываемый от нуля индекс для кнопки, связанной с указанным идентификатором команды.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды, связанный с кнопкой.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс для кнопки или-1, если указанный идентификатор команды является недопустимым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






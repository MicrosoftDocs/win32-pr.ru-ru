---
title: Сообщение TB_COMMANDTOINDEX (Коммктрл. h)
description: Возвращает отсчитываемый от нуля индекс для кнопки, связанной с указанным идентификатором команды.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- элементы управления Windows сообщений TB_COMMANDTOINDEX
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
ms.openlocfilehash: ea21f7436745ff3b6a8d69df4c2be43e59fc82e8e4e934302cddb71c9d342e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670397"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






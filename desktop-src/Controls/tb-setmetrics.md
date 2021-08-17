---
title: Сообщение TB_SETMETRICS (Коммктрл. h)
description: Задает метрики элемента управления ToolBar.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- элементы управления Windows сообщений TB_SETMETRICS
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c152d0fd1bfef894b1d54db768984697ebef2c9b82ac6d2663401363a338b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967914"
---
# <a name="tb_setmetrics-message"></a>\_Сообщение СЕТМЕТРИКС ТБ

Задает метрики элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Структура [**тбметрикс**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) , содержащая метрики панели инструментов, которые необходимо задать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






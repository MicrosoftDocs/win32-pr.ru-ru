---
title: Сообщение TB_GETMETRICS (Коммктрл. h)
description: Извлекает метрики элемента управления ToolBar.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- Элементы управления Windows для TB_GETMETRICS сообщений
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892341"
---
# <a name="tb_getmetrics-message"></a>\_Сообщение о НЕметриках ТБ

Извлекает метрики элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тбметрикс**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) , которая получает метрики панели инструментов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






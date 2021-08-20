---
title: Сообщение TB_GETHOTIMAGELIST (Коммктрл. h)
description: Извлекает список изображений, используемый элементом управления Toolbar для показа кнопок.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- элементы управления Windows сообщений TB_GETHOTIMAGELIST
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168517"
---
# <a name="tb_gethotimagelist-message"></a>\_Сообщение ЖЕСОТИМАЖЕЛИСТ ТБ

Извлекает список изображений, используемый элементом управления Toolbar для показа кнопок.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на список изображений, используемый элементом управления для показа активных кнопок, или **значение NULL** , если список горячих образов не задан.

## <a name="remarks"></a>Remarks

Кнопка находится в активном положении при наведении на нее курсора. Элементы управления "панель инструментов" должны иметь [**стиль \_ списка**](toolbar-control-and-button-styles.md) [**тбстиле \_ Flat**](toolbar-control-and-button-styles.md) или тбстиле, чтобы иметь активные элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






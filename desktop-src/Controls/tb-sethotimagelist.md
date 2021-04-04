---
title: Сообщение TB_SETHOTIMAGELIST (Коммктрл. h)
description: Задает список изображений, который будет использоваться элементом управления Toolbar для показа кнопок.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Элементы управления Windows для TB_SETHOTIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989063"
---
# <a name="tb_sethotimagelist-message"></a>\_Сообщение СЕСОТИМАЖЕЛИСТ ТБ

Задает список изображений, который будет использоваться элементом управления Toolbar для показа кнопок.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Обрабатываемый набор изображений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для списка изображений, который ранее использовался для вывода кнопок с кнопками, или **значение NULL** , если список изображений ранее не был задан.

## <a name="remarks"></a>Комментарии

Кнопка находится в активном положении при наведении на нее курсора. Элементы управления "панель инструментов" должны иметь [**стиль \_ списка**](toolbar-control-and-button-styles.md) [**тбстиле \_ Flat**](toolbar-control-and-button-styles.md) или тбстиле, чтобы иметь активные элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






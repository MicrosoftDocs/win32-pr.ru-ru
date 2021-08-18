---
title: Сообщение TB_SETHOTIMAGELIST (Коммктрл. h)
description: Задает список изображений, который будет использоваться элементом управления Toolbar для показа кнопок.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- элементы управления Windows сообщений TB_SETHOTIMAGELIST
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
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318854"
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

## <a name="remarks"></a>Remarks

Кнопка находится в активном положении при наведении на нее курсора. Элементы управления "панель инструментов" должны иметь [**стиль \_ списка**](toolbar-control-and-button-styles.md) [**тбстиле \_ Flat**](toolbar-control-and-button-styles.md) или тбстиле, чтобы иметь активные элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






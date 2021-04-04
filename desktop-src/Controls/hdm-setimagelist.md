---
title: Сообщение HDM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений существующему элементу управления "заголовок". Вы можете явно отправить это сообщение или использовать макрос Header \_ сетимажелист или Header \_ сетстатеимажелист.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Элементы управления Windows для HDM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988596"
---
# <a name="hdm_setimagelist-message"></a>\_Сообщение СЕТИМАЖЕЛИСТ HDM

Присваивает список изображений существующему элементу управления "заголовок". Вы можете явно отправить это сообщение или использовать макрос [**Header \_ Сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) или [**Header \_ сетстатеимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .

## <a name="parameters"></a>Параметры

<dl> <dt>*wParam*</dt> <dd>Одно из следующих значений:

| Значение                                                                                                                                                      | Значение                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**ХДСИЛ, \_ Обычная**</dt> </dl> | Указывает, что это стандартный список изображений.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**\_состояние хдсил**</dt> </dl>    | Указывает, что это список изображений состояния.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер для списка изображений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер в список изображений, ранее связанный с элементом управления. Возвращает **значение NULL** при сбое или если список изображений не был задан ранее.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






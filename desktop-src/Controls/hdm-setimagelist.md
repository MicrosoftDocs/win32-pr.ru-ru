---
title: Сообщение HDM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений существующему элементу управления "заголовок". Вы можете явно отправить это сообщение или использовать макрос Header \_ сетимажелист или Header \_ сетстатеимажелист.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- элементы управления Windows сообщений HDM_SETIMAGELIST
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
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435814"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






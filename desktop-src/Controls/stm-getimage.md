---
title: Сообщение STM_GETIMAGE (Winuser. h)
description: Приложение отправляет сообщение STM- \_ Image для получения маркера изображения (значка или точечного рисунка), связанного со статическим элементом управления.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Элементы управления Windows для STM_GETIMAGE сообщений
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071177"
---
# <a name="stm_getimage-message"></a>\_Сообщение STM

Приложение отправляет сообщение **STM- \_ Image** для получения маркера изображения (значка или точечного рисунка), связанного со статическим элементом управления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает тип извлекаемого изображения. Этот параметр может принимать одно из следующих значений:



| Значение                                                                                                                                                                     | Значение                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_точечный рисунок изображения**</dt> </dl>                | Массив.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**\_курсор изображения**</dt> </dl>                | Набора.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**\_ЕНХМЕТАФИЛЕ изображения**</dt> </dl> | Расширенный метафайл.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_значок изображения**</dt> </dl>                      | Значок.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это обработчик изображения, если таковой имеется; в противном случае он имеет **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**STM \_ сетимаже**](stm-setimage.md)
</dt> </dl>

 

 






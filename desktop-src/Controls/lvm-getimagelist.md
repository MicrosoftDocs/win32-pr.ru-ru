---
title: Сообщение LVM_GETIMAGELIST (Коммктрл. h)
description: Получает маркер для списка изображений, используемого для отображения элементов списка. Это сообщение можно отправить явным образом или с помощью \_ макроса ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Элементы управления Windows для LVM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136414"
---
# <a name="lvm_getimagelist-message"></a>Сообщение LVM/ \_ ImageList

Получает маркер для списка изображений, используемого для отображения элементов списка. Это сообщение можно отправить явным образом или с помощью макроса [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Список изображений для извлечения. Этот параметр может принимать одно из следующих значений:



| Значение                                                                                                                                                                     | Значение                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**ЛВСИЛ, \_ Обычная**</dt> </dl>                | Список изображений с большими значками.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**ЛВСИЛ \_ малый**</dt> </dl>                   | Список изображений с мелкими значками.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**\_состояние лвсил**</dt> </dl>                   | Список изображений с изображениями состояний.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**ЛВСИЛ \_ грауфеадер**</dt> </dl> | Список изображений для заголовка группы.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер в указанный список изображений в случае успешного выполнения или **значение NULL** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






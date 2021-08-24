---
title: Сообщение LVM_GETIMAGELIST (Коммктрл. h)
description: Получает маркер для списка изображений, используемого для отображения элементов списка. Это сообщение можно отправить явным образом или с помощью \_ макроса ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- элементы управления Windows сообщений LVM_GETIMAGELIST
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
ms.openlocfilehash: 339de36c85b4a5d39476a93cde71cbc6db23d1bc08946d3ce2d1ab1b5a4cb926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540814"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






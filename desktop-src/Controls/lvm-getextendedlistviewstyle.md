---
title: Сообщение LVM_GETEXTENDEDLISTVIEWSTYLE (Коммктрл. h)
description: Возвращает расширенные стили, используемые в данный момент для данного элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетекстендедлиствиевстиле ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- элементы управления Windows сообщений LVM_GETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968304"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>\_Сообщение LVM жетекстендедлиствиевстиле

Возвращает расширенные стили, используемые в данный момент для данного элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать макрос [**\_ жетекстендедлиствиевстиле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **DWORD** , представляющий стили, используемые в данный момент для данного элемента управления "представление списка". Это значение может быть сочетанием [расширенных стилей List-View](extended-list-view-styles.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






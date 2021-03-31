---
title: Сообщение LVM_GETEXTENDEDLISTVIEWSTYLE (Коммктрл. h)
description: Возвращает расширенные стили, используемые в данный момент для данного элемента управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетекстендедлиствиевстиле ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Элементы управления Windows для LVM_GETEXTENDEDLISTVIEWSTYLE сообщений
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071119"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






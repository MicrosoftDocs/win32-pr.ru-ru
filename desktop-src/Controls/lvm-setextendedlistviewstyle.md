---
title: Сообщение LVM_SETEXTENDEDLISTVIEWSTYLE (Коммктрл. h)
description: Задает расширенные стили в элементах управления "представление списка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView сетекстендедлиствиевстиле или ListView \_ сетекстендедлиствиевстиликс.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- элементы управления Windows сообщений LVM_SETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077284"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>\_Сообщение LVM сетекстендедлиствиевстиле

Задает расширенные стили в элементах управления "представление списка". Это сообщение можно отправить явным образом или воспользоваться макросом [**ListView \_ Сетекстендедлиствиевстиле**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) или [**ListView \_ сетекстендедлиствиевстиликс**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение **типа DWORD** , указывающее, какие стили в *lParam* должны быть затронуты. Этот параметр может быть сочетанием [**расширенных стилей List-View**](extended-list-view-styles.md). Будут изменены только расширенные стили в параметре *wParam* . Все остальные стили будут поддерживаться по мере их возникновения. Если этот параметр равен нулю, будут затронуты все стили в *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Значение **типа DWORD** , указывающее набор расширенных стилей элементов управления "представление списка". Этот параметр может быть сочетанием [**расширенных стилей List-View**](extended-list-view-styles.md). Стили, которые не заданы, но указаны в параметре *wParam*, удаляются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , содержащее предыдущие стили элемента управления "список" расширенного представления списка.

## <a name="remarks"></a>Remarks

Параметр *wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей. Например, если передать [**LVS \_ ex \_ фуллровселект**](extended-list-view-styles.md) для *wParam* и 0 для *lParam*, то стиль **LVS \_ ex \_ фуллровселект** будет сброшен, но все остальные стили останутся прежними.

В целях обратной совместимости макрос [**\_ сетекстендедлиствиевстиле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) не был обновлен для использования *wParam*. Чтобы использовать значение *wParam* , используйте макрос [**\_ сетекстендедлиствиевстиликс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

Если это сообщение используется для установки [**\_ \_ флажка LVS ex**](extended-list-view-styles.md) , все ранее установленные индексы изображений состояния будут удалены. Все флажки будут инициализированы с непроверенным состоянием. Индекс изображения состояния содержится в битах 12 – 15 элемента **State** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






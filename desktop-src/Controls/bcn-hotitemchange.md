---
title: Код уведомления BCN_HOTITEMCHANGE (Коммктрл. h)
description: Уведомляет владельца элемента управления "Кнопка", что указатель мыши вводит или выходит за пределы клиентской области элемента управления "Кнопка". Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения WM \_ Notify.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071464"
---
# <a name="bcn_hotitemchange-notification-code"></a>\_Код уведомления ХОТИТЕМЧАНЖЕ BCN

Уведомляет владельца элемента управления "Кнопка", что указатель мыши вводит или выходит за пределы клиентской области элемента управления "Кнопка". Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмбчотитем**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






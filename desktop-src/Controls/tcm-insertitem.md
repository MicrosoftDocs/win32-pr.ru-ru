---
title: Сообщение TCM_INSERTITEM (Коммктрл. h)
description: Вставляет новую вкладку в элемент управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- элементы управления Windows сообщений TCM_INSERTITEM
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829105"
---
# <a name="tcm_insertitem-message"></a>\_Сообщение INSERTITEM TCM

Вставляет новую вкладку в элемент управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс новой вкладки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , указывающую атрибуты вкладки. Члены этой структуры, **двстате** и **двстатемаск** , игнорируются этим сообщением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс новой вкладки, если она выполнена успешно, или значение-1 в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TCM \_ ИНСЕРТИТЕМВ** (Юникод) и **TCM \_ инсертитема** (ANSI)<br/>             |



 

 






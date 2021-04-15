---
title: Сообщение TCM_INSERTITEM (Коммктрл. h)
description: Вставляет новую вкладку в элемент управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Элементы управления Windows для TCM_INSERTITEM сообщений
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
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654665"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **TCM \_ ИНСЕРТИТЕМВ** (Юникод) и **TCM \_ инсертитема** (ANSI)<br/>             |



 

 






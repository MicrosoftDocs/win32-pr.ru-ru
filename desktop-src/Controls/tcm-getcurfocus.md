---
title: Сообщение TCM_GETCURFOCUS (Коммктрл. h)
description: Возвращает индекс элемента, который находится в фокусе ввода в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл жеткурфокус.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- элементы управления Windows сообщений TCM_GETCURFOCUS
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 694fb64b033d279292a687c39959925a68999c0b232c847bdf6ec6b476c725e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104944"
---
# <a name="tcm_getcurfocus-message"></a>\_Сообщение ЖЕТКУРФОКУС TCM

Возвращает индекс элемента, который находится в фокусе ввода в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ жеткурфокус**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента вкладки, который находится в фокусе.

## <a name="remarks"></a>Remarks

Элемент, имеющий фокус, может отличаться от выбранного элемента.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






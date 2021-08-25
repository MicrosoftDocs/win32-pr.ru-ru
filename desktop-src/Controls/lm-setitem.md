---
title: Сообщение LM_SETITEM (Коммктрл. h)
description: Задает состояния и атрибуты элемента.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- элементы управления Windows сообщений LM_SETITEM
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062804"
---
# <a name="lm_setitem-message"></a>\_Сообщение СЕТИТЕМ LM

Задает состояния и атрибуты элемента.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен иметь **значение NULL**. </dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-litem">литем</a> , содержащую новые состояния и атрибуты, необходимые для ссылки. </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если сообщение завершается с ошибкой при установке указанных значений и атрибутов.

## <a name="remarks"></a>Remarks

С сообщением [**LM- \_ Item**](lm-getitem.md) можно получить доступ к ссылкам только через числовой индекс, возвращенный в **iLink** члене [**литем**](/windows/win32/api/commctrl/ns-commctrl-litem). Обращение по ссылке через имя идентификатора, возвращенное в **сзид** , не поддерживается.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comctl32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






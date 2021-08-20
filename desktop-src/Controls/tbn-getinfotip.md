---
title: Код уведомления TBN_GETINFOTIP (Коммктрл. h)
description: Извлекает сведения о всплывающей подсказке для элемента панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6adb47a940ce6795047a1aca8bb7cbdc0899a142c132ab8f6f39e6bb089f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077908"
---
# <a name="tbn_getinfotip-notification-code"></a>\_Код уведомления ТБН жетинфотип

Извлекает сведения о всплывающей подсказке для элемента панели инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтбжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) , содержащую сведения об элементе и получающую сведения о всплывающих подсказках.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется элементом управления.

## <a name="remarks"></a>Remarks

Поддержка подсказки на панели инструментов позволяет отображать подсказки для элементов, имеющих размер ИНФОТИПСИЗЕ символов. Если этот код уведомления не обрабатывается, панель инструментов будет использовать текст элемента для подсказки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБН \_ ЖЕТИНФОТИПВ** (Юникод) и **ТБН \_ жетинфотипа** (ANSI)<br/>             |



 

 






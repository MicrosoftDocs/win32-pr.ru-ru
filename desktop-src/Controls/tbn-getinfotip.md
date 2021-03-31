---
title: Код уведомления TBN_GETINFOTIP (Коммктрл. h)
description: Извлекает сведения о всплывающей подсказке для элемента панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP кода уведомления элементы управления Windows
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
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071369"
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

## <a name="remarks"></a>Комментарии

Поддержка подсказки на панели инструментов позволяет отображать подсказки для элементов, имеющих размер ИНФОТИПСИЗЕ символов. Если этот код уведомления не обрабатывается, панель инструментов будет использовать текст элемента для подсказки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБН \_ ЖЕТИНФОТИПВ** (Юникод) и **ТБН \_ жетинфотипа** (ANSI)<br/>             |



 

 






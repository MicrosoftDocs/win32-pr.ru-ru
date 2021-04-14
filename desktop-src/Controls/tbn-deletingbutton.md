---
title: Сообщение TBN_DELETINGBUTTON (Коммктрл. h)
description: Посылается элементом управления ToolBar при удалении кнопки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Элементы управления Windows для TBN_DELETINGBUTTON сообщений
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533896"
---
# <a name="tbn_deletingbutton-message"></a>\_Сообщение ТБН делетингбуттон

Посылается элементом управления ToolBar при удалении кнопки. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) , содержащую сведения об удаляемой кнопке. Для этого кода уведомления допустимы только элементы **HDR** и **Член iItem** этой структуры. Элемент **Член iItem** этой структуры содержит идентификатор команды удаляемой кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 






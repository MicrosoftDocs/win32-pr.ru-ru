---
title: Сообщение TB_GETOBJECT (Коммктрл. h)
description: Получает интерфейс IDropTarget для элемента управления ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Элементы управления Windows для TB_GETOBJECT сообщений
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136815"
---
# <a name="tb_getobject-message"></a>\_Сообщение об ОБЪЕКТЕ ТБ

Получает [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) для элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор запрашиваемого интерфейса. Это значение должно указывать на **IID \_ интерфейс IDropTarget**.

</dd> <dt>

*lParam* 
</dt> <dd>

Адрес, получающий указатель интерфейса. При возникновении ошибки в этот адрес помещается **пустой** указатель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** , указывающее на успешное выполнение или сбой операции.

## <a name="remarks"></a>Комментарии

Панель инструментов [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) используется панелью инструментов, когда объекты перетаскиваются на него или отбрасываются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 


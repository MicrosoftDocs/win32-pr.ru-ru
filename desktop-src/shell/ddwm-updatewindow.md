---
description: Указывает, что окно удаления изображения будет обновляться с использованием новых данных ДРОПДЕСКРИПТИОН.
title: Сообщение DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032842"
---
# <a name="ddwm_updatewindow-message"></a>\_Сообщение ддвм упдатевиндов

Указывает, что окно удаления изображения будет обновляться с использованием новых данных [**дропдескриптион**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

ДДВМ \_ упдатевиндов определяется как WM \_ User + 3.

При изменении состояния операции удаления (например, в ответ на клавишу-модификатор)[**интерфейс IDropTarget::D раговер**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) возвращает новое значение [**Дропеффект**](../com/dropeffect-constants.md) (это **дропеффект** может также быть получено с помощью [**идропсаурце:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)). В ответ приложение обновляет структуру [**дропдескриптион**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) целевого объекта перетаскивания на новое значение [**дропимажетипе**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) , которое указывает на оформление, применяемое к визуальному элементу окна перетаскивания; Например, указывает, что файл копируется, а не перемещен, или что объект не может быть удален в это расположение. Однако визуальные элементы не обновляются, пока объект не получит сообщение **ддвм \_ упдатевиндов** .

Формат буфера обмена [драгвиндов](clipboard.md) предоставляет **HWND** окна, перетащив получателя, в отправителя сообщения **ддвм \_ упдатевиндов** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 

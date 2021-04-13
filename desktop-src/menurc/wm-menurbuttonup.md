---
title: Сообщение WM_MENURBUTTONUP (Winuser. h)
description: Посылается, когда пользователь отпускает правую кнопку мыши, когда курсор находится над пунктом меню.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341350"
---
# <a name="wm_menurbuttonup-message"></a>\_Сообщение МЕНУРБУТТОНУП WM

Посылается, когда пользователь отпускает правую кнопку мыши, когда курсор находится над пунктом меню.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс элемента меню, в котором была отжата правая кнопка мыши.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер меню, содержащего элемент.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сообщение **WM \_ менурбуттонуп** позволяет приложениям предоставлять контекстно-зависимое меню, которое также называется контекстным меню для пункта меню, указанного в этом сообщении. Чтобы отобразить контекстное меню для пункта меню, вызовите функцию [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) с **\_ рекурсией TPM**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о меню](menus.md)
</dt> </dl>

 

 






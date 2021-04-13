---
title: Сообщение WM_UNINITMENUPOPUP (Winuser. h)
description: Посылается при уничтожении раскрывающегося меню или подменю.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535543"
---
# <a name="wm_uninitmenupopup-message"></a>\_Сообщение УНИНИТМЕНУПОПУП WM

Посылается при уничтожении раскрывающегося меню или подменю.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер меню

</dd> <dt>

*lParam* 
</dt> <dd>

Слово в высоком порядке указывает на удаленное меню. В настоящее время этот параметр может иметь только значение **MF \_ сисмену** (меню "окно").

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если приложение получает сообщение [**WM \_ инитменупопуп**](wm-initmenupopup.md) , оно получит сообщение **WM \_ унинитменупопуп** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 


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
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971793"
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

## <a name="remarks"></a>Remarks

Если приложение получает сообщение [**WM \_ инитменупопуп**](wm-initmenupopup.md) , оно получит сообщение **WM \_ унинитменупопуп** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



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

 


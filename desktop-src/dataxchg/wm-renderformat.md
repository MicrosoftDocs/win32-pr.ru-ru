---
title: Сообщение WM_RENDERFORMAT (Winuser. h)
description: Отправляется владельцу буфера обмена, если он имеет отложенную визуализацию определенного формата буфера обмена и если приложение запрашивает данные в этом формате.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545313"
---
# <a name="wm_renderformat-message"></a>\_Сообщение RENDERFORMAT WM

Отправляется владельцу буфера обмена, если он имеет отложенную визуализацию определенного формата буфера обмена и если приложение запрашивает данные в этом формате. Владелец буфера обмена должен визуализировать данные в указанном формате и поместить их в буфер обмена, вызвав функцию [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[Формат буфера обмена](standard-clipboard-formats.md) для подготовки к просмотру.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

При ответе на сообщение **WM \_ RENDERFORMAT** владелец буфера обмена не должен открывать буфер обмена перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). Открытие буфера обмена не является обязательным, прежде чем поместить данные в ответ на **WM \_ RENDERFORMAT**, и любая попытка открыть буфер обмена завершится ошибкой, так как буфер обмена в настоящий момент остается открытым приложением, которое запросило отправку формата.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ рендераллформатс**](wm-renderallformats.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> </dl>

 

 






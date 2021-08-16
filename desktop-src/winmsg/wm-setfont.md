---
description: Задает шрифт, используемый элементом управления при рисовании текста.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Сообщение WM_SETFONT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199940"
---
# <a name="wm_setfont-message"></a>\_Сообщение СЕТФОНТ WM

Задает шрифт, используемый элементом управления при рисовании текста.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер для шрифта (**хфонт**). Если этот параметр имеет **значение NULL**, элемент управления использует системный шрифт по умолчанию для рисования текста.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово *lParam* в низком порядке указывает, должен ли элемент управления перерисоваться сразу после установки шрифта. Если этот параметр имеет **значение true**, элемент управления перерисовывает сам себя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Сообщение **WM \_ сетфонт** применяется ко всем элементам управления, а не только к тем, которые находятся в диалоговых окнах.

Самое лучшее время, когда владелец элемента управления диалогового окна задает шрифт элемента управления, — когда он получает сообщение [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) . Приложение должно вызвать функцию [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) , чтобы удалить шрифт, когда он больше не нужен; Например, после уничтожения элемента управления.

Размер элемента управления не изменяется в результате получения этого сообщения. Чтобы избежать усечения текста, который не умещается в границах элемента управления, приложение должно исправить размер окна элемента управления до того, как оно установит шрифт.

Когда в диалоговом окне используется [стиль \_ сетфонт DS](../dlgbox/about-dialog-boxes.md) для задания текста в элементах управления, система перед созданием элементов управления отправляет сообщение **WM \_ сетфонт** в процедуру диалогового окна. Приложение может создать диалоговое окно, содержащее \_ стиль DS сетфонт, вызвав одну из следующих функций:

-   [**креатедиалогиндирект**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**креатедиалогиндиректпарам**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**диалогбоксиндирект**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**диалогбоксиндиректпарам**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**креатедиалогиндирект**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**креатедиалогиндиректпарам**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**диалогбоксиндирект**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**диалогбоксиндиректпарам**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**длгтемплате**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**макелпарам**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM, \_ Шрифт**](wm-getfont.md)
</dt> <dt>

[**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 

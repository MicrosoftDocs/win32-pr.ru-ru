---
title: Автоматическое изменение размера элементов управления Rich Edit
description: Приложение может изменить размер элемента управления Rich Edit при необходимости, чтобы его размер всегда совпадал с его содержимым.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef3fa798da0a7747464d42535c638f437154124dd76b0324add35b5ba01931a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921724"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Автоматическое изменение размера элементов управления Rich Edit

Приложение может изменить размер элемента управления Rich Edit при необходимости, чтобы его размер всегда совпадал с его содержимым. Форматированный элемент управления "поле ввода" поддерживает такие функции, которые называются *ненижними* , отправляя его родительское окно с кодом уведомления [en \_ рекуестресизе](en-requestresize.md) всякий раз, когда изменяется размер содержимого элемента управления.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="automatically-resize-a-rich-edit-control"></a>Автоматическое изменение размера элемента управления Rich Edit

При обработке кода уведомления [en \_ рекуестресизе](en-requestresize.md) приложение должно изменить размер элемента управления на измерения в указанной структуре [**рекресизе**](/windows/desktop/api/Richedit/ns-richedit-reqresize) . Приложение также может перемещать любые сведения, расположенные рядом с элементом управления, чтобы обеспечить изменение высоты элемента управления. Чтобы изменить размер элемента управления, можно использовать функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Вы можете принудительно применить неформатированный элемент управления "поле с небольшими значениями" для отправки кода уведомления [en \_ рекуестресизе](en-requestresize.md) с помощью сообщения [**EM \_ рекуестресизе**](em-requestresize.md) . Это сообщение может быть полезно при обработке сообщения [**о \_ размере WM**](/windows/desktop/winmsg/wm-size) .

## <a name="remarks"></a>Remarks

Чтобы получить коды уведомлений [en \_ рекуестресизе](en-requestresize.md) , необходимо включить уведомление с помощью сообщения [EM \_ SETEVENTMASK](em-seteventmask.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[демонстрация Windows стандартных элементов управления (кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
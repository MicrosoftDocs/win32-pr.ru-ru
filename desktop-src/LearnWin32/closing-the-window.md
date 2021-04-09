---
title: Закрытие окна
description: Когда пользователь закрывает окно, это действие запускает последовательность сообщений окна.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890656"
---
# <a name="closing-the-window"></a>Закрытие окна

Когда пользователь закрывает окно, это действие запускает последовательность сообщений окна.

Пользователь может закрыть окно приложения, нажав кнопку **Закрыть** или воспользовавшись сочетанием клавиш, например ALT + F4. Любое из этих действий приводит к тому, что окно получает сообщение [**\_ закрытия WM**](/windows/desktop/winmsg/wm-close) . Сообщение **\_ закрытия WM** дает возможность запросить пользователя перед закрытием окна. Если вы действительно хотите закрыть окно, вызовите функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . В противном случае просто возвращает ноль из сообщения **\_ закрытия WM** , и операционная система пропустит это сообщение и не уничтожит окно.

Ниже приведен пример того, как программа может работать с [**WM \_ Close**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

В этом примере функция [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) показывает модальное диалоговое окно, содержащее кнопки **ОК** и **Отмена** . Если пользователь нажмет кнопку **ОК**, программа вызывает [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow). В противном случае, если пользователь нажимает кнопку **Отмена**, вызов **дестройвиндов** пропускается, а окно остается открытым. В любом случае возвращается нуль, чтобы указать, что сообщение обработано.

Если вы хотите закрыть окно без запроса пользователя, можно просто вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) без вызова [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). Однако в этом случае есть ярлык. Помните, что [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выполняет действие по умолчанию для любого сообщения окна. В случае с [**WM \_ Close**](/windows/desktop/winmsg/wm-close) **дефвиндовпрок** автоматически вызывает **дестройвиндов**. Это означает, что если вы пропускаете сообщение **\_ закрытия WM** в операторе **switch** , окно уничтожается по умолчанию.

Когда окно собирается уничтожиться, оно получает сообщение [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) . Это сообщение отправляется после удаления окна с экрана, но до возникновения уничтожения (в частности, перед уничтожением дочерних окон).

В главном окне приложения вы обычно отвечаете на [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) , вызывая [**посткуитмессаже**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

В разделе [оконных сообщений](window-messages.md) мы видели, что [**посткуитмессаже**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) помещает в очередь сообщений сообщение [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) , что приводит к завершению цикла обработки сообщений.

Ниже приведена типичная схема обработки сообщений [**WM \_ Close**](/windows/desktop/winmsg/wm-close) и [**WM \_ destroy**](/windows/desktop/winmsg/wm-destroy) .

![блок диаграмма, показывающий, как работать с \- сообщениями WM Close и WM \- destroy](images/wmclose01.png)

## <a name="next"></a>Следующая

[Управление состоянием приложения](managing-application-state-.md)
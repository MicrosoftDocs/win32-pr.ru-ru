---
description: Начиная с Windows Vista, технология Tablet PC поддерживает сенсорный ввод на планшетных ПК с дигитайзерами с поддержкой сенсорного ввода. Эта поддержка включает в себя усовершенствованный пользовательский интерфейс, помогающий нацеливание и командные окна при использовании пальца для ввода.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Поддержка сенсорного ввода в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702475"
---
# <a name="touch-input-support-in-windows-vista"></a>Поддержка сенсорного ввода в Windows Vista

Начиная с Windows Vista, технология Tablet PC поддерживает сенсорный ввод на планшетных ПК с дигитайзерами с поддержкой сенсорного ввода. Эта поддержка включает в себя усовершенствованный пользовательский интерфейс, помогающий нацеливание и командные окна при использовании пальца для ввода.

## <a name="touch-digitizer-support"></a>Поддержка сенсорного дигитайзера

### <a name="pen-and-touch-input-not-exclusive"></a>Входные данные пера и сенсорного ввода не являются эксклюзивными

Не представим, что перо и сенсорный ввод являются взаимоисключающими в приложениях [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)и [**RealTimeStylus**](realtimestylus-class.md) .

В Windows Vista, когда система распознает перо, она не учитывает сенсорный ввод. Это значит, что касание завершается и начинается рисование пера. Так как это может измениться в будущем, код не должен рассчитывать на то, что перо и сенсорный ввод являются взаимоисключающими.

### <a name="other-mouse-message-sources"></a>Другие источники сообщений мыши

Существуют и другие источники сообщений мыши, даже если пользователь взаимодействует только с помощью пальца или пера. Источники включают сенсорные панели, а также перемещение, предназначенное для того, чтобы приложение, расположенное за многослойным окном, было осведомлено о том, что мышь перемещается над приложением.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Включение и отключение пользовательского интерфейса сенсорного ввода

Вы можете включить или отключить сенсорный ввод пользовательского интерфейса в зависимости от требований приложения. Для этого следует перехватить сообщения окна операционной системы в процедуре окна и изменить сообщение Windows. Переопределите [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) в приложении, чтобы перехватить эти сообщения. В следующем \# псевдо-коде на языке C показано, как включить и отключить сенсорный ввод пользовательского интерфейса. В коде также показано использование той же методики для отключения жеста нажатия и удерживания. Этот метод также работает для отключения пера.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Windows Touch](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 

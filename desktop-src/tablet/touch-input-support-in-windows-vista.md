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
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="e8264-104">Поддержка сенсорного ввода в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8264-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="e8264-105">Начиная с Windows Vista, технология Tablet PC поддерживает сенсорный ввод на планшетных ПК с дигитайзерами с поддержкой сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="e8264-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="e8264-106">Эта поддержка включает в себя усовершенствованный пользовательский интерфейс, помогающий нацеливание и командные окна при использовании пальца для ввода.</span><span class="sxs-lookup"><span data-stu-id="e8264-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="e8264-107">Поддержка сенсорного дигитайзера</span><span class="sxs-lookup"><span data-stu-id="e8264-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="e8264-108">Входные данные пера и сенсорного ввода не являются эксклюзивными</span><span class="sxs-lookup"><span data-stu-id="e8264-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="e8264-109">Не представим, что перо и сенсорный ввод являются взаимоисключающими в приложениях [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)и [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e8264-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="e8264-110">В Windows Vista, когда система распознает перо, она не учитывает сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="e8264-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="e8264-111">Это значит, что касание завершается и начинается рисование пера.</span><span class="sxs-lookup"><span data-stu-id="e8264-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="e8264-112">Так как это может измениться в будущем, код не должен рассчитывать на то, что перо и сенсорный ввод являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e8264-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="e8264-113">Другие источники сообщений мыши</span><span class="sxs-lookup"><span data-stu-id="e8264-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="e8264-114">Существуют и другие источники сообщений мыши, даже если пользователь взаимодействует только с помощью пальца или пера.</span><span class="sxs-lookup"><span data-stu-id="e8264-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="e8264-115">Источники включают сенсорные панели, а также перемещение, предназначенное для того, чтобы приложение, расположенное за многослойным окном, было осведомлено о том, что мышь перемещается над приложением.</span><span class="sxs-lookup"><span data-stu-id="e8264-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="e8264-116">Включение и отключение пользовательского интерфейса сенсорного ввода</span><span class="sxs-lookup"><span data-stu-id="e8264-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="e8264-117">Вы можете включить или отключить сенсорный ввод пользовательского интерфейса в зависимости от требований приложения.</span><span class="sxs-lookup"><span data-stu-id="e8264-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="e8264-118">Для этого следует перехватить сообщения окна операционной системы в процедуре окна и изменить сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="e8264-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="e8264-119">Переопределите [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) в приложении, чтобы перехватить эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="e8264-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="e8264-120">В следующем \# псевдо-коде на языке C показано, как включить и отключить сенсорный ввод пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e8264-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="e8264-121">В коде также показано использование той же методики для отключения жеста нажатия и удерживания.</span><span class="sxs-lookup"><span data-stu-id="e8264-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="e8264-122">Этот метод также работает для отключения пера.</span><span class="sxs-lookup"><span data-stu-id="e8264-122">This method also works for disabling the stylus.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e8264-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e8264-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8264-124">Windows Touch</span><span class="sxs-lookup"><span data-stu-id="e8264-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 

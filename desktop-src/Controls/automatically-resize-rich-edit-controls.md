---
title: Автоматическое изменение размера элементов управления Rich Edit
description: Приложение может изменить размер элемента управления Rich Edit при необходимости, чтобы его размер всегда совпадал с его содержимым.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070712"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="50a72-103">Автоматическое изменение размера элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="50a72-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="50a72-104">Приложение может изменить размер элемента управления Rich Edit при необходимости, чтобы его размер всегда совпадал с его содержимым.</span><span class="sxs-lookup"><span data-stu-id="50a72-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="50a72-105">Форматированный элемент управления "поле ввода" поддерживает такие функции, которые называются *ненижними* , отправляя его родительское окно с кодом уведомления [en \_ рекуестресизе](en-requestresize.md) всякий раз, когда изменяется размер содержимого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50a72-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="50a72-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="50a72-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="50a72-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="50a72-107">Technologies</span></span>

-   [<span data-ttu-id="50a72-108">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="50a72-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="50a72-109">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="50a72-109">Prerequisites</span></span>

-   <span data-ttu-id="50a72-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="50a72-110">C/C++</span></span>
-   <span data-ttu-id="50a72-111">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="50a72-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="50a72-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="50a72-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="50a72-113">Автоматическое изменение размера элемента управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="50a72-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="50a72-114">При обработке кода уведомления [en \_ рекуестресизе](en-requestresize.md) приложение должно изменить размер элемента управления на измерения в указанной структуре [**рекресизе**](/windows/desktop/api/Richedit/ns-richedit-reqresize) .</span><span class="sxs-lookup"><span data-stu-id="50a72-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="50a72-115">Приложение также может перемещать любые сведения, расположенные рядом с элементом управления, чтобы обеспечить изменение высоты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50a72-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="50a72-116">Чтобы изменить размер элемента управления, можно использовать функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="50a72-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="50a72-117">Вы можете принудительно применить неформатированный элемент управления "поле с небольшими значениями" для отправки кода уведомления [en \_ рекуестресизе](en-requestresize.md) с помощью сообщения [**EM \_ рекуестресизе**](em-requestresize.md) .</span><span class="sxs-lookup"><span data-stu-id="50a72-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="50a72-118">Это сообщение может быть полезно при обработке сообщения [**о \_ размере WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="50a72-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a72-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50a72-119">Remarks</span></span>

<span data-ttu-id="50a72-120">Чтобы получить коды уведомлений [en \_ рекуестресизе](en-requestresize.md) , необходимо включить уведомление с помощью сообщения [EM \_ SETEVENTMASK](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="50a72-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50a72-121">См. также</span><span class="sxs-lookup"><span data-stu-id="50a72-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50a72-122">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="50a72-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="50a72-123">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="50a72-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
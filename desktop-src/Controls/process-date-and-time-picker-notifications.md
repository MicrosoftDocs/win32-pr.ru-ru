---
title: Обработка уведомлений средства выбора даты и времени
description: В этом разделе показано, как обрабатывать уведомления средства выбора даты и времени.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424184"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="c375e-103">Обработка уведомлений средства выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="c375e-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="c375e-104">В этом разделе показано, как обрабатывать уведомления средства выбора даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c375e-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c375e-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="c375e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c375e-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="c375e-106">Technologies</span></span>

-   [<span data-ttu-id="c375e-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="c375e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c375e-108">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="c375e-108">Prerequisites</span></span>

-   <span data-ttu-id="c375e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c375e-109">C/C++</span></span>
-   <span data-ttu-id="c375e-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="c375e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c375e-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="c375e-111">Instructions</span></span>


<span data-ttu-id="c375e-112">Элемент управления "Выбор даты и времени" (DTP) отправляет сообщения уведомления родительскому окну, когда события, обычно активируемые вводом от пользователя, происходят в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="c375e-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="c375e-113">Приложение должно включать код для определения типа сообщения уведомления и ответа соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="c375e-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="c375e-114">Если вы планируете использовать поля обратного вызова с элементами управления DTP в приложении, необходимо подготовиться к обработке кодов уведомлений [ДТН \_ форматкуери](dtn-formatquery.md), [ДТН \_ ](dtn-format.md)и [ДТН \_ вмкэйдовн](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="c375e-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="c375e-115">Дополнительные сведения о полях обратного вызова см. в разделе [поля обратного вызова](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c375e-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="c375e-116">В следующем примере кода C++ определяется сообщение уведомления, отправленное элементом управления DTP, и вызывается соответствующая определяемая приложением функция.</span><span class="sxs-lookup"><span data-stu-id="c375e-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="c375e-117">В следующих разделах приведены примеры кода, иллюстрирующие процесс обработки уведомлений, которые отображаются в этом примере.</span><span class="sxs-lookup"><span data-stu-id="c375e-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="c375e-118">Разделы</span><span class="sxs-lookup"><span data-stu-id="c375e-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c375e-119">Обработка \_ уведомления ДТН датетимечанже</span><span class="sxs-lookup"><span data-stu-id="c375e-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="c375e-120">Обработка \_ уведомления ДТН форматкуери</span><span class="sxs-lookup"><span data-stu-id="c375e-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="c375e-121">Обработка \_ уведомления формата ДТН</span><span class="sxs-lookup"><span data-stu-id="c375e-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="c375e-122">Обработка \_ уведомления ДТН вмкэйдовн</span><span class="sxs-lookup"><span data-stu-id="c375e-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="c375e-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c375e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c375e-124">Уведомления средства выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="c375e-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="c375e-125">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="c375e-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c375e-126">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="c375e-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="c375e-127">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="c375e-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





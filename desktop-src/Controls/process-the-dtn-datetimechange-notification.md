---
title: Обработка уведомления DTN_DATETIMECHANGE
description: В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988030"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="63e14-103">Обработка \_ уведомления ДТН датетимечанже</span><span class="sxs-lookup"><span data-stu-id="63e14-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="63e14-104">В этом разделе показано, как обрабатывать уведомления об изменениях, внесенных пользователем, к элементу выбора даты и времени (DTP).</span><span class="sxs-lookup"><span data-stu-id="63e14-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="63e14-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="63e14-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="63e14-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="63e14-106">Technologies</span></span>

-   [<span data-ttu-id="63e14-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="63e14-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="63e14-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="63e14-108">Prerequisites</span></span>

-   <span data-ttu-id="63e14-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="63e14-109">C/C++</span></span>
-   <span data-ttu-id="63e14-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="63e14-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="63e14-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="63e14-111">Instructions</span></span>


<span data-ttu-id="63e14-112">Элемент управления DTP отправляет код [уведомления \_ датетимечанже ДТН](dtn-datetimechange.md) каждый раз, когда происходит изменение.</span><span class="sxs-lookup"><span data-stu-id="63e14-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="63e14-113">Например, это уведомление будет создано при изменении пользователем одного из полей в элементе управления или в случае, если элемент управления установлен в стиль [**\_ шовноне DTS**](date-and-time-picker-control-styles.md) , когда пользователь изменяет состояние флажка элемента управления.</span><span class="sxs-lookup"><span data-stu-id="63e14-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="63e14-114">Приложение должно содержать код для обработки сообщений ДТН \_ датетимечанже, которые отправляются элементом управления DTP.</span><span class="sxs-lookup"><span data-stu-id="63e14-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="63e14-115">Следующий пример кода C++ представляет собой определяемую приложением функцию, предназначенную для указания состояния элемента управления DTP, для которого задан стиль **\_ Шовноне служб DTS** .</span><span class="sxs-lookup"><span data-stu-id="63e14-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="63e14-116">См. также</span><span class="sxs-lookup"><span data-stu-id="63e14-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63e14-117">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="63e14-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="63e14-118">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="63e14-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="63e14-119">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="63e14-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





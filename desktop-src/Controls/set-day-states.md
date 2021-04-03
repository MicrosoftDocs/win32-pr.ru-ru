---
title: Как задать состояния дней
description: В этом разделе показано, как задать сведения о состоянии дня. Элемент управления "календарь месяца" использует сведения о состоянии дня для определения того, как он рисует определенные дни внутри элемента управления.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988026"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="e866e-104">Как задать состояния дней</span><span class="sxs-lookup"><span data-stu-id="e866e-104">How to Set Day States</span></span>

<span data-ttu-id="e866e-105">В этом разделе показано, как задать сведения о состоянии дня.</span><span class="sxs-lookup"><span data-stu-id="e866e-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="e866e-106">Элемент управления "календарь месяца" использует сведения о состоянии дня для определения того, как он рисует определенные дни внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e866e-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="e866e-107">Элементы управления "месячный календарь", в которых используются состояния дня поддержки в стиле [**\_ дайстате MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e866e-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="e866e-108">Сведения о состоянии дня выражаются как 32-разрядный тип данных [**монсдайстате**](monthdaystate.md).</span><span class="sxs-lookup"><span data-stu-id="e866e-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="e866e-109">Каждый бит в **монсдайстате** битовых битах (от 0 до 30) указывает состояние дня в месяце.</span><span class="sxs-lookup"><span data-stu-id="e866e-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="e866e-110">Если бит включен, соответствующий день выводится полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="e866e-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e866e-111">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="e866e-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e866e-112">Технологии</span><span class="sxs-lookup"><span data-stu-id="e866e-112">Technologies</span></span>

-   [<span data-ttu-id="e866e-113">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="e866e-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e866e-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e866e-114">Prerequisites</span></span>

-   <span data-ttu-id="e866e-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="e866e-115">C/C++</span></span>
-   <span data-ttu-id="e866e-116">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="e866e-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e866e-117">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e866e-117">Instructions</span></span>


<span data-ttu-id="e866e-118">Приложение может явно задавать сведения о состоянии дня путем отправки сообщения [**MCM \_ сетдайстате**](mcm-setdaystate.md) или с помощью соответствующего макроса, [**монскал \_ сетдайстате**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="e866e-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="e866e-119">Однако информация о состоянии дня обычно задается в ответ на код уведомления [МКН \_ жетдайстате](mcn-getdaystate.md) , который отправляется при необходимости обновления элемента управления, так как, например, другой месяц прокручивается в представлении.</span><span class="sxs-lookup"><span data-stu-id="e866e-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="e866e-120">В следующем примере кода показано, как обработать код уведомления [МКН \_ жетдайстате](mcn-getdaystate.md) в обработчике сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e866e-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="e866e-121">Он обрабатывает МКН \_ жетдайстате, указывая, что первый и пятнадцатый день каждого видимого месяца должны быть выделены.</span><span class="sxs-lookup"><span data-stu-id="e866e-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="e866e-122">Элемент **кдайстате** структуры [**нмдайстате**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) указывает количество значений [**монсдайстате**](monthdaystate.md) , необходимых в массиве, для которого задан произвольный максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="e866e-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="e866e-123">Затем в коде выполняется циклическая установка соответствующих битов в каждом допустимом элементе массива с помощью определяемого приложением макроса **болддай** .</span><span class="sxs-lookup"><span data-stu-id="e866e-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a><span data-ttu-id="e866e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e866e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e866e-125">Справочник по управлению календарем месяца</span><span class="sxs-lookup"><span data-stu-id="e866e-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e866e-126">Элементы управления "календарь месяца"</span><span class="sxs-lookup"><span data-stu-id="e866e-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="e866e-127">Использование элементов управления "календарь месяца"</span><span class="sxs-lookup"><span data-stu-id="e866e-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





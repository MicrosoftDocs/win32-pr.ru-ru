---
title: Как реализовать подсказки для значков строки состояния
description: Неагрессивный способ отобразить пояснительное сообщение для значка строки состояния — реализовать подсказку. При щелчке всплывающая подсказка исчезает, но можно также указать значение времени ожидания.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488361"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="50083-104">Как реализовать подсказки для значков строки состояния</span><span class="sxs-lookup"><span data-stu-id="50083-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="50083-105">Неагрессивный способ отобразить пояснительное сообщение для значка строки состояния — реализовать подсказку.</span><span class="sxs-lookup"><span data-stu-id="50083-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="50083-106">При щелчке всплывающая подсказка исчезает, но можно также указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="50083-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="50083-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="50083-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="50083-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="50083-108">Technologies</span></span>

-   [<span data-ttu-id="50083-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="50083-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="50083-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="50083-110">Prerequisites</span></span>

-   <span data-ttu-id="50083-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="50083-111">C/C++</span></span>
-   <span data-ttu-id="50083-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="50083-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="50083-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="50083-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="50083-114">Реализация подсказок для значков строки состояния</span><span class="sxs-lookup"><span data-stu-id="50083-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="50083-115">В следующем фрагменте кода показано, как добавить всплывающую подсказку к значку строки состояния.</span><span class="sxs-lookup"><span data-stu-id="50083-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="50083-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50083-116">Remarks</span></span>

<span data-ttu-id="50083-117">Подробное описание строки состояния см. [на панели задач](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="50083-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="50083-118">Чтобы отобразить всплывающую подсказку, необходимо установить \_ флаг сведений о nЕсли в структуре [**нотификондата**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) и использовать члены **сзинфо** и **утимеаут** для указания текста подсказки и времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="50083-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50083-119">См. также</span><span class="sxs-lookup"><span data-stu-id="50083-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50083-120">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="50083-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 
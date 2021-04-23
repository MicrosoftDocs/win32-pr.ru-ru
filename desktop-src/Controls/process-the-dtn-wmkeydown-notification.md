---
title: Обработка уведомления DTN_WMKEYDOWN
description: В этом разделе показано, как обработать \_ уведомление ДТН вмкэйдовн. Обработка этого кода уведомления позволяет владельцу элемента управления предоставлять определенные ответы на нажатия клавиш в полях обратного вызова элемента управления.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891260"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="61052-104">Обработка \_ уведомления ДТН вмкэйдовн</span><span class="sxs-lookup"><span data-stu-id="61052-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="61052-105">В этом разделе показано, как обработать уведомление [ДТН \_ вмкэйдовн](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="61052-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="61052-106">Обработка этого кода уведомления позволяет владельцу элемента управления предоставлять определенные ответы на нажатия клавиш в полях обратного вызова элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61052-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61052-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="61052-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61052-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="61052-108">Technologies</span></span>

-   [<span data-ttu-id="61052-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="61052-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="61052-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="61052-110">Prerequisites</span></span>

-   <span data-ttu-id="61052-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="61052-111">C/C++</span></span>
-   <span data-ttu-id="61052-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="61052-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="61052-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="61052-113">Instructions</span></span>


<span data-ttu-id="61052-114">Элементы управления "Выбор даты и времени" (DTP) отправляют сообщение [ \_ вмкэйдовн ДТН](dtn-wmkeydown.md) , чтобы сообщить о том, что пользователь ввел ввод в поле обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="61052-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="61052-115">Если вы хотите эмулировать те же ответы клавиатуры, которые поддерживаются для стандартных полей DTP или предоставляющих пользовательские ответы, приложение должно содержать код для работы с этим уведомлением.</span><span class="sxs-lookup"><span data-stu-id="61052-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="61052-116">Следующий пример кода C++ представляет собой определяемую приложением функцию, которая обрабатывает уведомление [ДТН \_ вмкэйдовн](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="61052-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="61052-117">**Предупреждение системы безопасности:** Неправильное использование **лстркмп** может привести к нарушению безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="61052-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="61052-118">Например, перед вызовом **лстркмп** в следующем примере кода следует убедиться, что две строки завершаются нулем.</span><span class="sxs-lookup"><span data-stu-id="61052-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="61052-119">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: Microsoft Windows Controls](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="61052-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="61052-120">См. также</span><span class="sxs-lookup"><span data-stu-id="61052-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61052-121">Использование элементов управления "Выбор даты и времени"</span><span class="sxs-lookup"><span data-stu-id="61052-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="61052-122">Справочник по элементу выбора даты и времени</span><span class="sxs-lookup"><span data-stu-id="61052-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="61052-123">Выбор даты и времени</span><span class="sxs-lookup"><span data-stu-id="61052-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





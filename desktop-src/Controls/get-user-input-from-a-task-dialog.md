---
title: Получение пользовательского ввода из диалогового окна задачи
description: Чтобы выполнить задачу, пользователи отправляют сведения о задачах в приложение, настраивая элементы управления в диалоговом окне задачи, а затем щелкая кнопку команды (обычно это нормально).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987938"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="74238-103">Получение пользовательского ввода из диалогового окна задачи</span><span class="sxs-lookup"><span data-stu-id="74238-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="74238-104">Чтобы выполнить задачу, пользователи отправляют сведения о задачах в приложение, настраивая элементы управления в диалоговом окне задачи, а затем щелкая кнопку команды (обычно это **нормально**).</span><span class="sxs-lookup"><span data-stu-id="74238-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="74238-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="74238-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="74238-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="74238-106">Technologies</span></span>

-   [<span data-ttu-id="74238-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="74238-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="74238-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="74238-108">Prerequisites</span></span>

-   <span data-ttu-id="74238-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="74238-109">C/C++</span></span>
-   <span data-ttu-id="74238-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="74238-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="74238-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="74238-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="74238-112">Получение вводимых пользователем данных из диалогового окна задачи</span><span class="sxs-lookup"><span data-stu-id="74238-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="74238-113">Можно выбрать кнопку, которая была нажата, изучив параметр *пнбуттон* вызывающей функции.</span><span class="sxs-lookup"><span data-stu-id="74238-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="74238-114">Можно также определить выбранный переключатель в параметре *пнрадиобуттон* параметра [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)и состояние флажка проверки из параметра *пфверификатионфлагчеккед* .</span><span class="sxs-lookup"><span data-stu-id="74238-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="74238-115">Нажатие кнопок и гиперссылок получаются функцией [*таскдиалогкаллбаккпрок*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) в форме нажатия [ \_ кнопки ТДН \_](tdn-button-clicked.md) , а [ТДН \_ гиперссылки \_ —](tdn-hyperlink-clicked.md) на уведомления.</span><span class="sxs-lookup"><span data-stu-id="74238-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="74238-116">Если функция обратного вызова возвращает значение S \_ ОК после обработки уведомления кнопки, диалоговое окно задачи закрывается, а идентификатор команды возвращается в *пнбуттон*.</span><span class="sxs-lookup"><span data-stu-id="74238-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="74238-117">Если вы возвращаете \_ значение false или не имеете функции обратного вызова, диалоговое окно задачи остается открытым.</span><span class="sxs-lookup"><span data-stu-id="74238-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74238-118">См. также</span><span class="sxs-lookup"><span data-stu-id="74238-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74238-119">Использование диалоговых окон задач</span><span class="sxs-lookup"><span data-stu-id="74238-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 
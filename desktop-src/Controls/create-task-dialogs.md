---
title: Создание диалоговых окон задач
description: Диалоговое окно задачи создается и отображается с помощью функции Таскдиалог или функции Таскдиалогиндирект.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067548"
---
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="74da7-103">Создание диалоговых окон задач</span><span class="sxs-lookup"><span data-stu-id="74da7-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="74da7-104">Диалоговое окно задачи создается и отображается с помощью функции [**таскдиалог**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) или функции [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="74da7-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="74da7-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="74da7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="74da7-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="74da7-106">Technologies</span></span>

-   [<span data-ttu-id="74da7-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="74da7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="74da7-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="74da7-108">Prerequisites</span></span>

-   <span data-ttu-id="74da7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="74da7-109">C/C++</span></span>
-   <span data-ttu-id="74da7-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="74da7-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="74da7-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="74da7-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="74da7-112">таскдиалог</span><span class="sxs-lookup"><span data-stu-id="74da7-112">TaskDialog</span></span>

<span data-ttu-id="74da7-113">Функция **таскдиалог** подходит для простых диалоговых окон, которые представляют текстовую информацию и запрашивают стандартный вариант.</span><span class="sxs-lookup"><span data-stu-id="74da7-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="74da7-114">Эта функция создания не поддерживает индикаторы выполнения, флажки, нижние колонтитулы, кнопки развертывания и свертывания, настраиваемые кнопки и переключатели.</span><span class="sxs-lookup"><span data-stu-id="74da7-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="74da7-115">таскдиалогиндирект</span><span class="sxs-lookup"><span data-stu-id="74da7-115">TaskDialogIndirect</span></span>

<span data-ttu-id="74da7-116">Функция **таскдиалогиндирект** является более мощной, поддерживающей все доступные элементы интерфейса, а также позволяет записывать события в процедуру обратного вызова, чтобы приложение может обновить индикатор выполнения или ответить на щелчок гиперссылки или кнопки.</span><span class="sxs-lookup"><span data-stu-id="74da7-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74da7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="74da7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74da7-118">Использование диалоговых окон задач</span><span class="sxs-lookup"><span data-stu-id="74da7-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 





---
title: Поддержка локализации для стандартных элементов управления
description: В этом разделе описывается поддержка национальных языков, встроенных в общие элементы управления.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986269"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="38f89-103">Поддержка локализации для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="38f89-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="38f89-104">В этом разделе описывается поддержка национальных языков, встроенных в общие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="38f89-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="38f89-105">Встроенная поддержка национальных языков упрощает реализацию локализованных приложений.</span><span class="sxs-lookup"><span data-stu-id="38f89-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="38f89-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="38f89-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="38f89-107">Указание языка для общих элементов управления</span><span class="sxs-lookup"><span data-stu-id="38f89-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="38f89-108">Указание языка для элементов управления в диалоговом окне</span><span class="sxs-lookup"><span data-stu-id="38f89-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="38f89-109">См. также</span><span class="sxs-lookup"><span data-stu-id="38f89-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="38f89-110">Указание языка для общих элементов управления</span><span class="sxs-lookup"><span data-stu-id="38f89-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="38f89-111">Если необходимо указать язык для общих элементов управления, отличающихся от языка системы, вызовите [**инитмуилангуаже**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="38f89-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="38f89-112">Язык, заданный этой функцией, применяется только к процессу, из которого вызывается функция.</span><span class="sxs-lookup"><span data-stu-id="38f89-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="38f89-113">Чтобы определить, какой язык в данный момент используется общими элементами управления, вызовите [**жетмуилангуаже**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="38f89-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="38f89-114">Он возвращает значение, заданное предыдущим вызовом метода [**инитмуилангуаже**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="38f89-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="38f89-115">Возвращаемый язык — это тот, который был указан для процесса, из которого он вызывается.</span><span class="sxs-lookup"><span data-stu-id="38f89-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="38f89-116">Если **инитмуилангуаже** не был вызван или был вызван из другого процесса, **жетмуилангуаже** вернет значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38f89-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="38f89-117">Указание языка для элементов управления в диалоговом окне</span><span class="sxs-lookup"><span data-stu-id="38f89-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="38f89-118">В отличие от стандартных элементов управления, стандартные элементы управления, такие как кнопки или поля ввода, по умолчанию не используют текущий язык системы.</span><span class="sxs-lookup"><span data-stu-id="38f89-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="38f89-119">Элемент управления "Шрифт" машинного кода — это невидимый элемент управления, который работает в фоновом режиме, что позволяет использовать стандартные элементы управления диалогового окна для вывода текущего языка системы.</span><span class="sxs-lookup"><span data-stu-id="38f89-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="38f89-120">Чтобы использовать собственный элемент управления шрифта, выполните следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="38f89-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="38f89-121">Инициализируйте собственный элемент управления шрифта путем вызова [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="38f89-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="38f89-122">Установите элемент **двикк** структуры [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) , на который указывает *лпинитктрлс* , в класс ICC \_ нативефнтктл \_ .</span><span class="sxs-lookup"><span data-stu-id="38f89-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="38f89-123">Добавьте элемент управления в скрипт ресурсов для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="38f89-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="38f89-124">Установите один или несколько из следующих флагов стиля, чтобы указать, какие элементы управления будут затронуты.</span><span class="sxs-lookup"><span data-stu-id="38f89-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="38f89-125">Flag</span><span class="sxs-lookup"><span data-stu-id="38f89-125">Flag</span></span>              | <span data-ttu-id="38f89-126">Применяется к</span><span class="sxs-lookup"><span data-stu-id="38f89-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="38f89-127">\_изменение NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-127">NFS\_EDIT</span></span>         | <span data-ttu-id="38f89-128">Изменить элементы управления</span><span class="sxs-lookup"><span data-stu-id="38f89-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="38f89-129">\_СТАТИЧЕСКАЯ NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-129">NFS\_STATIC</span></span>       | <span data-ttu-id="38f89-130">Статические элементы управления</span><span class="sxs-lookup"><span data-stu-id="38f89-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="38f89-131">\_ЛИСТКОМБО NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="38f89-132">Элементы управления List, ComboBox, List-View и ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="38f89-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="38f89-133">\_кнопка NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="38f89-134">Элементы управления "Кнопка"</span><span class="sxs-lookup"><span data-stu-id="38f89-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="38f89-135">\_все NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-135">NFS\_ALL</span></span>          | <span data-ttu-id="38f89-136">Все элементы управления</span><span class="sxs-lookup"><span data-stu-id="38f89-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="38f89-137">\_УСЕФОНТАССОК NFS</span><span class="sxs-lookup"><span data-stu-id="38f89-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="38f89-138">Восточно-Азиатская платформа.</span><span class="sxs-lookup"><span data-stu-id="38f89-138">East Asian platform.</span></span> <span data-ttu-id="38f89-139">Элемент управления использует функцию сопоставления шрифтов вместо переключения на собственный шрифт.</span><span class="sxs-lookup"><span data-stu-id="38f89-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="38f89-140">Все остальные платформы игнорируют его.</span><span class="sxs-lookup"><span data-stu-id="38f89-140">All other platforms ignore it.</span></span> <span data-ttu-id="38f89-141">Это не рекомендуется для Windows Vista и не поддерживается в комктл V6.</span><span class="sxs-lookup"><span data-stu-id="38f89-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="38f89-142">Это существует в комктл V5 для устаревших причин.</span><span class="sxs-lookup"><span data-stu-id="38f89-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="38f89-143">В следующем примере показано, как добавить собственный элемент управления шрифта в скрипт ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38f89-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="38f89-144">Это приводит к тому, что элементы управления, списки и поля со списком в диалоговом окне заменяют текст на текущем языке системы.</span><span class="sxs-lookup"><span data-stu-id="38f89-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="38f89-145">См. также</span><span class="sxs-lookup"><span data-stu-id="38f89-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f89-146">Общие сведения об элементах управления</span><span class="sxs-lookup"><span data-stu-id="38f89-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 





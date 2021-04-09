---
title: Использование диалоговых окон
description: Используйте диалоговые окна для вывода сведений и запроса ввода от пользователя.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Пользовательский интерфейс Windows, окна
- Пользовательский интерфейс Windows, диалоговые окна
- окна, диалоговые окна
- диалоговые окна, сведения
- диалоговые окна, отображение
- модальные диалоговые окна
- безрежимные диалоговые окна
- диалоговые окна, модальные
- диалоговые окна, немодальные
- диалоговые окна, инициализация
- шаблоны диалоговых окон
- диалоговые окна, шаблоны
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070433"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="6a86d-115">Использование диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="6a86d-115">Using Dialog Boxes</span></span>

<span data-ttu-id="6a86d-116">Используйте диалоговые окна для вывода сведений и запроса ввода от пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a86d-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="6a86d-117">Приложение загружает и Инициализирует диалоговое окно, обрабатывает входные данные пользователя и уничтожает диалоговое окно, когда пользователь завершает задачу.</span><span class="sxs-lookup"><span data-stu-id="6a86d-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="6a86d-118">Процесс обработки диалоговых окон зависит от того, является ли диалоговое окно модальным или немодальным.</span><span class="sxs-lookup"><span data-stu-id="6a86d-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="6a86d-119">Модальное диалоговое окно требует, чтобы пользователь закрыл диалоговое окно перед активацией другого окна в приложении.</span><span class="sxs-lookup"><span data-stu-id="6a86d-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="6a86d-120">Однако пользователь может активировать Windows в разных приложениях.</span><span class="sxs-lookup"><span data-stu-id="6a86d-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="6a86d-121">Немодальное диалоговое окно не требует немедленного ответа от пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a86d-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="6a86d-122">Он аналогичен главному окну, содержащему элементы управления.</span><span class="sxs-lookup"><span data-stu-id="6a86d-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="6a86d-123">В следующих разделах описывается использование обоих типов диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="6a86d-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="6a86d-124">Отображение окна сообщения</span><span class="sxs-lookup"><span data-stu-id="6a86d-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="6a86d-125">Создание модального диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="6a86d-126">Создание немодального диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="6a86d-127">Инициализация диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="6a86d-128">Создание шаблона в памяти</span><span class="sxs-lookup"><span data-stu-id="6a86d-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="6a86d-129">Отображение окна сообщения</span><span class="sxs-lookup"><span data-stu-id="6a86d-129">Displaying a Message Box</span></span>

<span data-ttu-id="6a86d-130">Простейшей формой модального диалогового окна является окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="6a86d-131">Большинство приложений используют окна сообщений для предупреждения пользователя об ошибках и для запроса инструкций о том, как продолжать работу после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="6a86d-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="6a86d-132">Создайте окно сообщения с помощью функции [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) или [**мессажебоксекс**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , указав сообщение и число и тип отображаемых кнопок.</span><span class="sxs-lookup"><span data-stu-id="6a86d-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="6a86d-133">Система создает модальное диалоговое окно, предоставляя собственный шаблон и процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="6a86d-134">После того, как пользователь закроет окно сообщения, **MessageBox** или **мессажебоксекс** возвращает значение, идентифицирующее кнопку, выбранную пользователем, чтобы закрыть окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="6a86d-135">В следующем примере приложение отображает окно сообщения, предлагающее пользователю ввести действие после возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="6a86d-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="6a86d-136">В окне сообщения отобразится сообщение с описанием условия ошибки и способами ее устранения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="6a86d-137">**\_ Данет** в стиле "МБ" направляет [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) для предоставления двух кнопок, с помощью которых пользователь может выбрать способ продолжения:</span><span class="sxs-lookup"><span data-stu-id="6a86d-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="6a86d-138">На следующем рисунке показаны выходные данные предыдущего примера кода:</span><span class="sxs-lookup"><span data-stu-id="6a86d-138">The following image shows the output from the preceding code example:</span></span>

![окно сообщения](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="6a86d-140">Создание модального диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="6a86d-141">Модальное диалоговое окно создается с помощью функции [**диалогбокс**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="6a86d-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="6a86d-142">Необходимо указать идентификатор или имя ресурса шаблона диалогового окна и указатель на процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="6a86d-143">Функция **диалогбокс** загружает шаблон, отображает диалоговое окно и обрабатывает все входные данные пользователя до тех пор, пока пользователь не закроет диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="6a86d-144">В следующем примере приложение отображает модальное диалоговое окно, когда пользователь нажимает кнопку " **удалить элемент** " из меню приложения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="6a86d-145">Диалоговое окно содержит элемент управления "поле ввода" (в котором пользователь вводит имя элемента) и кнопки  "ОК **" и "Отмена"** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="6a86d-146">Идентификаторы элементов управления для этих элементов управления имеют ИДЕНТИФИКАТОРы \_ ITEMNAME, идок и идканцел соответственно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="6a86d-147">Первая часть примера состоит из инструкций, которые создают модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="6a86d-148">Эти инструкции в процедуре окна для главного окна приложения создают диалоговое окно, когда система получает сообщение [**\_ команды WM**](/windows/desktop/menurc/wm-command) с \_ идентификатором меню IDM DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="6a86d-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="6a86d-149">Во второй части примера показана процедура диалогового окна, которая извлекает содержимое элемента управления "поле ввода" и закрывает диалоговое окно при получении **\_ командного сообщения WM** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="6a86d-150">Следующие инструкции создают модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="6a86d-151">Шаблон диалогового окна — это ресурс в исполняемом файле приложения с идентификатором ресурса DLG \_ DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="6a86d-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="6a86d-152">В этом примере приложение указывает его главное окно в качестве окна "владелец" для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="6a86d-153">Когда система первоначально отображает диалоговое окно, его расположение задается относительно верхнего левого угла клиентской области окна-владельца.</span><span class="sxs-lookup"><span data-stu-id="6a86d-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="6a86d-154">Приложение использует возвращаемое значение из [**диалогбокс**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) , чтобы определить, следует ли продолжить операцию или отменить ее.</span><span class="sxs-lookup"><span data-stu-id="6a86d-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="6a86d-155">В следующих инструкциях определяется процедура диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="6a86d-156">В этом примере процедура использует [**жетдлгитемтекст**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) для получения текущего текста из элемента управления Edit, идентифицируемого по идентификатору \_ ITEMNAME.</span><span class="sxs-lookup"><span data-stu-id="6a86d-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="6a86d-157">Затем процедура вызывает функцию [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) для задания возвращаемого значения диалогового окна как ИДОК или идканцел, в зависимости от полученного сообщения и для начала процесса закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="6a86d-158">Идентификаторы ИДОК и ИДКАНЦЕЛ соответствуют кнопкам **ОК** и **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="6a86d-159">После вызова метода **EndDialog** система отправляет дополнительные сообщения в процедуру для уничтожения диалогового окна и возвращает обратное значение диалогового окна функции, создавшей диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="6a86d-160">Создание немодального диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="6a86d-161">Можно создать немодальное диалоговое окно с помощью функции [**креатедиалог**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , указав идентификатор или имя ресурса шаблона диалогового окна, а также указатель на процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="6a86d-162">**Креатедиалог** загружает шаблон, создает диалоговое окно и при необходимости отображает его.</span><span class="sxs-lookup"><span data-stu-id="6a86d-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="6a86d-163">Приложение отвечает за получение и отправку сообщений о вводе пользователем в процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="6a86d-164">В следующем примере приложение отображает немодальное диалоговое окно (если оно еще не отображается), когда пользователь щелкает **"переход к** " из меню приложения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="6a86d-165">Диалоговое окно содержит элемент управления "поле ввода", флажок, а также кнопки " **ОК** " и **"Отмена"** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="6a86d-166">Шаблон диалогового окна — это ресурс в исполняемом файле приложения с идентификатором ресурса DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="6a86d-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="6a86d-167">Пользователь вводит номер строки в элементе управления "поле ввода" и устанавливает флажок, чтобы указать, что номер строки относится к текущей строке.</span><span class="sxs-lookup"><span data-stu-id="6a86d-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="6a86d-168">Идентификаторы элементов управления: \_ line ID, ID \_ АБСРЕЛ, ИДОК и идканцел.</span><span class="sxs-lookup"><span data-stu-id="6a86d-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="6a86d-169">Инструкции в первой части примера создают немодальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="6a86d-170">Эти инструкции в процедуре окна для главного окна приложения создают диалоговое окно, когда процедура окна получает сообщение [**\_ команды WM**](/windows/desktop/menurc/wm-command) с \_ идентификатором меню IDM, но только в том случае, если глобальная переменная еще не содержит допустимый обработчик.</span><span class="sxs-lookup"><span data-stu-id="6a86d-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="6a86d-171">Вторая часть примера — основной цикл обработки сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="6a86d-172">Цикл включает функцию [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) , чтобы убедиться, что пользователь может использовать интерфейс клавиатуры диалогового окна в этом немодальном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6a86d-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="6a86d-173">В третьей части примера приведена процедура диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="6a86d-174">Процедура извлекает содержимое элемента управления "поле ввода" и флажка, когда пользователь нажимает кнопку " **ОК** ".</span><span class="sxs-lookup"><span data-stu-id="6a86d-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="6a86d-175">Процедура уничтожает диалоговое окно, когда пользователь нажимает кнопку **Отмена** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="6a86d-176">В приведенных выше инструкциях [**креатедиалог**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) вызывается, только если не `hwndGoto` содержит допустимый обработчик окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="6a86d-177">Это гарантирует, что приложение не будет одновременно отображать два диалоговых окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="6a86d-178">Для поддержки этого метода процедура диалогового окна должна иметь значение **null** при уничтожении диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="6a86d-179">Цикл обработки сообщений для приложения состоит из следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="6a86d-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="6a86d-180">Цикл проверяет допустимость диалогового окна в диалоговом окне и вызывает функцию [**исдиалогмессаже**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) только в том случае, если этот маркер является допустимым.</span><span class="sxs-lookup"><span data-stu-id="6a86d-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="6a86d-181">**Исдиалогмессаже** обрабатывает сообщение только в том случае, если оно принадлежит диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="6a86d-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="6a86d-182">В противном случае возвращается **значение false** , и цикл отправляет сообщение в соответствующее окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="6a86d-183">В следующих инструкциях определяется процедура диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="6a86d-184">В приведенных выше инструкциях процедура обрабатывает сообщения [**\_ командной строки**](/windows/desktop/menurc/wm-command) [**WM \_ инитдиалог**](wm-initdialog.md) и WM.</span><span class="sxs-lookup"><span data-stu-id="6a86d-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="6a86d-185">Во время обработки **\_ Инитдиалог в WM** процедура Инициализирует этот флажок, передавая текущее значение глобальной переменной в [**чеккдлгбуттон**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span><span class="sxs-lookup"><span data-stu-id="6a86d-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="6a86d-186">Затем процедура возвращает **значение true** , чтобы система настроила фокус ввода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a86d-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="6a86d-187">Во время обработки [**\_ команд WM**](/windows/desktop/menurc/wm-command) это диалоговое окно закрывается только в том случае, если пользователь нажмет кнопку **Отмена** , то есть кнопку с идентификатором идканцел.</span><span class="sxs-lookup"><span data-stu-id="6a86d-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="6a86d-188">Процедура должна вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) , чтобы закрыть немодальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="6a86d-189">Обратите внимание, что процедура также задает для переменной **значение NULL** , чтобы убедиться, что другие инструкции, зависящие от этой переменной, работают правильно.</span><span class="sxs-lookup"><span data-stu-id="6a86d-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="6a86d-190">Если пользователь нажмет кнопку **ОК** , процедура получает текущее состояние флажка и назначает его переменной **фрелативе** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="6a86d-191">Затем она использует переменную для получения номера строки из элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="6a86d-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="6a86d-192">[**Жетдлгитеминт**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) преобразует текст в элементе управления "поле ввода" в целое число.</span><span class="sxs-lookup"><span data-stu-id="6a86d-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="6a86d-193">Значение **фрелативе** определяет, интерпретирует ли функция число как значение со знаком или без знака.</span><span class="sxs-lookup"><span data-stu-id="6a86d-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="6a86d-194">Если текст элемента управления "поле ввода" не является допустимым числом, **жетдлгитеминт** устанавливает значение переменной **fError** равным нулю.</span><span class="sxs-lookup"><span data-stu-id="6a86d-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="6a86d-195">Процедура проверяет это значение, чтобы определить, следует ли отображать сообщение об ошибке или выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="6a86d-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="6a86d-196">В случае ошибки процедура диалогового окна отправляет сообщение в элемент управления редактированием, направляя его для выбора текста в элементе управления, чтобы пользователь мог легко его заменить.</span><span class="sxs-lookup"><span data-stu-id="6a86d-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="6a86d-197">Если **жетдлгитеминт** не возвращает ошибку, процедура может либо выполнить запрошенную задачу, либо отправить сообщение в окно владельца, направляя его для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6a86d-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="6a86d-198">Инициализация диалогового окна</span><span class="sxs-lookup"><span data-stu-id="6a86d-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="6a86d-199">Вы Инициализирует диалоговое окно и его содержимое при обработке сообщения [**WM \_ инитдиалог**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6a86d-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="6a86d-200">Наиболее распространенной задачей является инициализация элементов управления для отражения текущих настроек диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="6a86d-201">Другой распространенной задачей является центрирование диалогового окна на экране или в окне его владельца.</span><span class="sxs-lookup"><span data-stu-id="6a86d-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="6a86d-202">Полезной задачей для некоторых диалоговых окон является установка фокуса ввода на указанный элемент управления вместо принятия фокуса ввода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a86d-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="6a86d-203">В следующем примере диалоговое окно обрабатывает диалоговое окно и устанавливает фокус ввода при обработке сообщения [**WM \_ инитдиалог**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="6a86d-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="6a86d-204">Для центрирования диалогового окна процедура извлекает прямоугольники окна для диалогового окна и окна владелец и вычисляет новую точку для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="6a86d-205">Чтобы установить фокус ввода, процедура проверяет параметр *wParam* , чтобы определить идентификатор фокуса ввода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a86d-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="6a86d-206">В приведенных выше инструкциях процедура [**использует функцию getHandler**](/windows/desktop/api/winuser/nf-winuser-getparent) для получения маркера окна-владельца для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="6a86d-207">Функция возвращает обработчик окна владельца в диалоговые окна, а родительский окно — в дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="6a86d-208">Поскольку приложение может создать диалоговое окно, не имеющее владельца, процедура проверяет возвращенный обработчик и использует функцию [**жетдесктопвиндов**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) для получения маркера окна рабочего стола при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6a86d-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="6a86d-209">После вычисления новой должности процедура использует функцию [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) для перемещения диалогового окна, указывая \_ верхнее значение HWND, чтобы убедиться, что диалоговое окно остается в верхней части окна владельца.</span><span class="sxs-lookup"><span data-stu-id="6a86d-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="6a86d-210">Перед установкой фокуса ввода процедура проверяет идентификатор элемента управления фокуса ввода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a86d-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="6a86d-211">Система передает маркер окна фокуса ввода по умолчанию в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6a86d-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="6a86d-212">Функция [**жетдлгктрлид**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) возвращает идентификатор элемента управления, идентифицируемого маркером окна.</span><span class="sxs-lookup"><span data-stu-id="6a86d-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="6a86d-213">Если идентификатор не соответствует правильному идентификатору, процедура использует функцию [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) для установки фокуса ввода.</span><span class="sxs-lookup"><span data-stu-id="6a86d-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="6a86d-214">Функция [**жетдлгитем**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) необходима для получения маркера окна требуемого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6a86d-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="6a86d-215">Создание шаблона в памяти</span><span class="sxs-lookup"><span data-stu-id="6a86d-215">Creating a Template in Memory</span></span>

<span data-ttu-id="6a86d-216">Приложения иногда адаптируют или изменяют содержимое диалоговых окон в зависимости от текущего состояния обрабатываемых данных.</span><span class="sxs-lookup"><span data-stu-id="6a86d-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="6a86d-217">В таких случаях нецелесообразно предоставлять все возможные шаблоны диалоговых окон в качестве ресурсов исполняемого файла приложения.</span><span class="sxs-lookup"><span data-stu-id="6a86d-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="6a86d-218">Но создание шаблонов в памяти обеспечивает большую гибкость при адаптации к любым обстоятельствам.</span><span class="sxs-lookup"><span data-stu-id="6a86d-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="6a86d-219">В следующем примере приложение создает шаблон в памяти для модального диалогового окна, содержащего сообщение и кнопки « **ОК** » и « **Справка** ».</span><span class="sxs-lookup"><span data-stu-id="6a86d-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="6a86d-220">В шаблоне диалогового окна все символьные строки, например диалоговые окна и заголовки кнопок, должны быть строками в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="6a86d-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="6a86d-221">В этом примере используется функция [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) для создания этих строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="6a86d-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="6a86d-222">Структуры [**длгитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) в шаблоне диалогового окна должны быть согласованы по границам **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="6a86d-223">Чтобы выстроить эти структуры, в этом примере используется вспомогательная подпрограммы, которая принимает входной указатель и возвращает ближайший указатель, выравниваемая по границе **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6a86d-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 
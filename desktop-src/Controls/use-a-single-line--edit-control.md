---
title: Создание элемента управления "изменение одной строки"
description: В этом разделе показано, как создать диалоговое окно, содержащее элемент управления "поле ввода" с одной строкой.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070867"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="7898f-103">Создание элемента управления "изменение одной строки"</span><span class="sxs-lookup"><span data-stu-id="7898f-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="7898f-104">В этом разделе показано, как создать диалоговое окно, содержащее элемент управления "поле ввода" с одной строкой.</span><span class="sxs-lookup"><span data-stu-id="7898f-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="7898f-105">Однострочный элемент управления "поле ввода" имеет стиль [**\_ пароля ES**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7898f-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="7898f-106">По умолчанию элементы управления "поле ввода" с этим стилем отображают звездочку для каждого введенного пользователем символа.</span><span class="sxs-lookup"><span data-stu-id="7898f-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="7898f-107">Однако в этом примере используется сообщение [**EM \_ сетпассвордчар**](em-setpasswordchar.md) для изменения символа по умолчанию с звездочки на знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="7898f-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="7898f-108">На следующем снимке экрана показано диалоговое окно после ввода пароля пользователем.</span><span class="sxs-lookup"><span data-stu-id="7898f-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![снимок экрана с диалоговым окном, содержащим элемент управления "поле ввода" с вводом пароля](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="7898f-110">Версия Comctl32.dll 6 не является распространяемой.</span><span class="sxs-lookup"><span data-stu-id="7898f-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="7898f-111">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="7898f-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="7898f-112">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7898f-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7898f-113">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="7898f-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7898f-114">Технологии</span><span class="sxs-lookup"><span data-stu-id="7898f-114">Technologies</span></span>

-   [<span data-ttu-id="7898f-115">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="7898f-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7898f-116">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7898f-116">Prerequisites</span></span>

-   <span data-ttu-id="7898f-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="7898f-117">C/C++</span></span>
-   <span data-ttu-id="7898f-118">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="7898f-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7898f-119">Инструкции</span><span class="sxs-lookup"><span data-stu-id="7898f-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="7898f-120">Шаг 1. Создание экземпляра диалогового окна "пароль".</span><span class="sxs-lookup"><span data-stu-id="7898f-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="7898f-121">В следующем примере кода C++ для создания модального диалогового окна используется функция Диалогбокс.</span><span class="sxs-lookup"><span data-stu-id="7898f-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="7898f-122">**\_ Пароль Идд** шаблона диалогового окна передается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="7898f-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="7898f-123">Он определяет, помимо прочего, стили окна, кнопки и размеры диалогового окна пароль.</span><span class="sxs-lookup"><span data-stu-id="7898f-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="7898f-124">Шаг 2. Инициализация диалогового окна и обработка входных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="7898f-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="7898f-125">Процедура Window в следующем примере Инициализирует диалоговое окно Password и обрабатывает сообщения уведомления и данные, вводимые пользователем.</span><span class="sxs-lookup"><span data-stu-id="7898f-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="7898f-126">Во время инициализации процедура окна изменяет символ пароля по умолчанию на **+** знак и устанавливает для кнопки по умолчанию значение **Cancel**.</span><span class="sxs-lookup"><span data-stu-id="7898f-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="7898f-127">Во время обработки пользовательского ввода процедура окна изменяет кнопку принудительной отправки по умолчанию с **Cancel** на **ОК** , как только пользователь введет текст в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="7898f-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="7898f-128">Если пользователь нажмет кнопку **ОК** , в процедуре Window используются сообщения [**EM \_ линеленгс**](em-linelength.md) и EM для [**получения \_**](em-getline.md) текста.</span><span class="sxs-lookup"><span data-stu-id="7898f-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a><span data-ttu-id="7898f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7898f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7898f-130">Сведения об элементах управления "Изменить"</span><span class="sxs-lookup"><span data-stu-id="7898f-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="7898f-131">Изменить ссылку на элемент управления</span><span class="sxs-lookup"><span data-stu-id="7898f-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7898f-132">Использование элементов управления Edit</span><span class="sxs-lookup"><span data-stu-id="7898f-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="7898f-133">Изменить элемент управления</span><span class="sxs-lookup"><span data-stu-id="7898f-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 
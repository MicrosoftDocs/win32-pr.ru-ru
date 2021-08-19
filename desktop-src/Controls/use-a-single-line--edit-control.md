---
title: Создание элемента управления "изменение одной строки"
description: В этом разделе показано, как создать диалоговое окно, содержащее элемент управления "поле ввода" с одной строкой.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597c3e611f53af56a42f837c4d85a43f97ff846e371314b130d72c568aaf860e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829123"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Создание элемента управления "изменение одной строки"

В этом разделе показано, как создать диалоговое окно, содержащее элемент управления "поле ввода" с одной строкой.

Однострочный элемент управления "поле ввода" имеет стиль [**\_ пароля ES**](edit-control-styles.md) . По умолчанию элементы управления "поле ввода" с этим стилем отображают звездочку для каждого введенного пользователем символа. Однако в этом примере используется сообщение [**EM \_ сетпассвордчар**](em-setpasswordchar.md) для изменения символа по умолчанию с звездочки на знак плюса (+). На следующем снимке экрана показано диалоговое окно после ввода пароля пользователем.

![снимок экрана с диалоговым окном, содержащим элемент управления "поле ввода" с вводом пароля](images/passworddlg.png)

> [!Note]  
> Версия Comctl32.dll 6 не является распространяемой. Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Шаг 1. Создание экземпляра диалогового окна "пароль".

В следующем примере кода C++ для создания модального диалогового окна используется функция Диалогбокс. **\_ Пароль Идд** шаблона диалогового окна передается в качестве параметра. Он определяет, помимо прочего, стили окна, кнопки и размеры диалогового окна пароль.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Шаг 2. Инициализация диалогового окна и обработка входных данных пользователя.

Процедура Window в следующем примере Инициализирует диалоговое окно Password и обрабатывает сообщения уведомления и данные, вводимые пользователем.

Во время инициализации процедура окна изменяет символ пароля по умолчанию на **+** знак и устанавливает для кнопки по умолчанию значение **Cancel**.

Во время обработки пользовательского ввода процедура окна изменяет кнопку принудительной отправки по умолчанию с **Cancel** на **ОК** , как только пользователь введет текст в поле ввода. Если пользователь нажмет кнопку **ОК** , в процедуре Window используются сообщения [**EM \_ линеленгс**](em-linelength.md) и EM для [**получения \_**](em-getline.md) текста.



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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об элементах управления "Изменить"](about-edit-controls.md)
</dt> <dt>

[Изменить ссылку на элемент управления](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Использование элементов управления Edit](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Изменить элемент управления](edit-controls.md)
</dt> </dl>

 

 
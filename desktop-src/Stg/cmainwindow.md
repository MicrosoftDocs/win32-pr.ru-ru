---
title: кмаинвиндов
description: Эта процедура показана в следующем примере кода.
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- кмаинвиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f67fd2a00bb6f3ab082499e5ca2a4a991a9fb33159a4f43c05923ae393efcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962471"
---
# <a name="cmainwindow"></a>кмаинвиндов

операционная система Microsoft Windows преобразует следующие действия пользователя в стандартные сообщения окна и отправляет их в основную процедуру в приложении **стоклиен** :

-   Пользователь нажимает левую кнопку мыши или выключатель в планшетных устройствах, чтобы начать последовательность рисования линий.
-   Пользователь нажимает и удерживает кнопку и перемещает мышь для рисования линии.
-   Последовательность заканчивается при отпускании левой кнопки мыши.

Эта процедура показана в следующем примере кода.

## <a name="cmainwindowwindowproc-stocliencpp"></a>Кмаинвиндов:: WindowProc (СТОКЛИЕН. CPP


```C++
LRESULT CMainWindow::WindowProc(
            UINT uMsg,
            WPARAM wParam,
            LPARAM lParam)
  {
    LRESULT lResult = FALSE;

    switch (uMsg)
    {
      case WM_CREATE:
        break;

      case WM_ACTIVATE:
        // A mouse click reactivates the paint procedure.
        // This is used to paint a new window when a user
        // selects a portion of the STOCLIEN window that is 
        // visible beneath another window. This message is  
        // sent in the WindowProc handle.
        if (WA_CLICKACTIVE == LOWORD(wParam))
          m_pGuiPaper->PaintWin();
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;

      case WM_SIZE:
        // Handle a resize of this window.
        m_wWidth = LOWORD(lParam);
        m_wHeight = HIWORD(lParam);
        // Inform CGuiPaper of the change.
        m_pGuiPaper->Resize(m_wWidth, m_wHeight);
        break;

      case WM_PAINT:
        // This is a message to repaint the window.
        {
          PAINTSTRUCT ps;

          if(BeginPaint(m_hWnd, &ps))
            EndPaint(m_hWnd, &ps);

          m_pGuiPaper->PaintWin();
        }
        break;

      case WM_LBUTTONDOWN:
        // Start sequence of ink drawing to the paper.
        m_pGuiPaper->InkStart(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_MOUSEMOVE:
        // Draw inking sequence data.
        m_pGuiPaper->InkDraw(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_LBUTTONUP:
        // Stop an ink drawing sequence.
        m_pGuiPaper->InkStop(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_COMMAND:
        // Dispatch and handle any Menu command messages received.
        lResult = DoMenu(wParam, lParam);
        break;

      case WM_CHAR:
        if (wParam == 0x1b)
        {
          // Exit this application if user presses the ESC key.
          ::PostMessage(m_hWnd, WM_CLOSE, 0, 0);
        }
        break;

      case WM_CLOSE:
        // The user selected Close on the main window System menu
        // or Exit on the File menu.
        // If there is unsaved ink data, then prompt
        // the user. If the user cancels, do not close the window.
        if (IDCANCEL == m_pGuiPaper->AskSave())
          break;
      case WM_QUIT:
        // When exiting the application, close any associated help
        // windows.
        // ::WinHelp(m_hWnd, m_szHelpFile, HELP_QUIT, 0);
      default:
        // If there are any messages that have not been handled,
        // send them to the default window procedure.
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;
    }

    return(lResult);
  }
```



Последовательность рисования линий начинается, когда сообщение WM \_ лбуттондовн доставляет данные о положении мыши.

Кмаинвиндов имеет указатель на объект Кгуипапер и вызывает метод [**кгуипапер:: инкстарт**](cguipaper-methods.md) для запуска последовательности рисования линии.

По мере перемещения указателя мыши на Draw в метод [кгуипапер:: инкдрав](cguipaper-methods.md) передаются последовательность отдельных сообщений **WM \_ MOUSEMOVE** , содержащих данные о положении мыши.

При отпускании левой кнопки мыши получается сообщение **WM \_ лбуттонуп** . Метод [кгуипапер:: инкстоп](cguipaper-methods.md) останавливает последовательность рисования линий.

 

 





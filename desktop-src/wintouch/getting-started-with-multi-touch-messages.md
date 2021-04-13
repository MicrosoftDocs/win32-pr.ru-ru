---
title: начало работы с сообщениями касания Windows
description: В этом разделе объясняются задачи, связанные с получением входных данных Windows Touch для работы в приложении.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Касание Windows, сообщения
- Касание Windows, регистрация для сенсорного ввода
- Касание Windows, тестирование входных дигитайзеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413100"
---
# <a name="getting-started-with-windows-touch-messages"></a>начало работы с сообщениями касания Windows

В этом разделе объясняются задачи, связанные с получением входных данных Windows Touch для работы в приложении.

При работе с сообщениями Windows Touch обычно выполняются следующие действия.

1.  Проверьте возможности входного дигитайзера.
2.  Зарегистрируйтесь для получения сообщений Windows Touch.
3.  Обработайте сообщения.

Для Windows Touch используется сообщение [**WM \_ Touch**](wm-touchdown.md). Это сообщение указывает различные состояния контакта с дигитайзером.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Тестирование возможностей входного дигитайзера

Функцию [жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) можно использовать для запроса возможностей входного дигитайзера путем передачи значения *ниндекс* в **SM \_ дигитайзере**. [Жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) возвращает битовое поле, которое указывает, готово ли устройство, поддерживает ли устройство перо или сенсорный ввод, является ли устройство ввода интегрированным или внешним, а также поддерживает ли устройство несколько входов (Windows Touch). В следующей таблице показаны биты для различных полей.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Значение | Стек готов | Множественный ввод | Зарезервировано | Зарезервировано | Внешнее перо | Интегрированное перо | Внешнее касание | Интегрированное касание |



 

Чтобы проверить результат команды для определенной функции, можно использовать побитовый оператор & и определенный бит, который тестируется. Например, чтобы протестировать Windows Touch, необходимо проверить, установлен ли бит седьмого порядка (0x40 в шестнадцатеричном формате). В следующем примере кода показано, как можно проверить эти значения.


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



В следующей таблице перечислены константы, определенные в Windows. h для тестирования сенсорных возможностей входного дигитайзера.



| Имя                   | Значение      | Описание                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Конфигурация ПЛАНШЕТа \_ \_ нет   | 0x00000000 | У входного дигитайзера нет возможностей сенсорного ввода.                                                                                                                                         |
| \_интегрированное \_ КАСАНИе NID | 0x00000001 | Для ввода используется интегрированный сенсорный дигитайзер.                                                                                                                                              |
| NID \_ внешнее \_ касание   | 0x00000002 | Для ввода используется внешний сенсорный дигитайзер.                                                                                                                                                |
| \_интегрированное \_ перо NID   | 0x00000004 | Для ввода используется интегрированный дигитайзер.                                                                                                                                                |
| \_внешнее \_ перо NID     | 0x00000008 | Для ввода используется внешний дигитайзер пера.                                                                                                                                                  |
| NID \_ Multi \_ input      | 0x00000040 | Для входных данных используется входной дигитайзер с поддержкой нескольких входов.                                                                                                                        |
| NID \_ Готово             | 0x00000080 | Входной дигитайзер готов для ввода. Если это значение не задано, это может означать, что служба планшета остановлена, дигитайзер не поддерживается или драйверы дигитайзера не установлены. |



 

Проверка значений NID \_ \* является удобным способом проверки возможностей компьютера пользователя, чтобы настроить приложение для использования сенсорного ввода, пера или не планшета. Например, если у вас есть динамический пользовательский интерфейс (UI) и вы хотите автоматически настроить некоторые из них, можно проверить \_ встроенное \_ касание NID, NID \_ Мультисенсорная и получить максимальное число касаний при первом запуске приложения пользователем.

> [!Note]  
> Существуют некоторые ограничения для SM \_ жетсистемметрикс. Например, Plug and Play не поддерживается. По этой причине следует соблюдать осторожность при использовании этой функции в качестве средства для постоянной конфигурации.

 

## <a name="registering-to-receive-windows-touch-input"></a>Регистрация для получения сенсорного ввода Windows

Перед получением сенсорного ввода Windows сначала приложения должны зарегистрироваться для получения сенсорного ввода Windows. Зарегистрировав окно приложения, приложение указывает, что оно совместимо с касанием. После того как приложение регистрирует свое окно, уведомления из драйвера Windows Touch пересылаются в приложение при вводе данных в окне. Когда приложение завершает работу, оно отменяет регистрацию своего окна для отключения уведомлений.

> [!Note]  
> [**WM \_ СЕНСОРные**](wm-touchdown.md) сообщения в настоящее время являются «жадными». После получения первого сообщения Touch в окне все сенсорные сообщения отправляются в это окно, пока фокус не будет получен другим окном.

 

> [!Note]  
> По умолчанию вы получаете [**сообщения \_ жестов WM**](wm-gesture.md) вместо сообщений [**WM \_ Touch**](wm-touchdown.md) . При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы перестанете получать **сообщения \_ жестов WM** .

 

В следующем коде показано, как приложение может зарегистрироваться для получения сообщений Windows Touch в приложении Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Обработка сообщений касания Windows

Вы можете управлять сообщениями Windows Touch из приложений в операционных системах Windows различными способами. При программировании приложения с графическим интерфейсом вы добавляете в `WndProc` функцию код, который обрабатывает интересующие сообщения. При программировании Microsoft Foundation Class (MFC) или управляемого приложения вы добавляете обработчики для интересующих сообщений. В следующем примере кода показано, как можно обрабатывать сенсорные сообщения из WndProc в приложении на базе Windows.


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





В следующем коде показано, как можно реализовать схему сообщений и обработчик сообщений. Обратите внимание, что сообщения должны быть объявлены в схеме сообщений, а затем должен быть реализован обработчик для этого сообщения. Например, в приложении MFC это можно объявить в коде диалогового окна. Обратите внимание, что `OnInitDialog` функция для диалогового окна должна содержать вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , например `RegisterTouchWindow(m_hWnd, 0)` .


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



Прикосновение к окну означает, что они появятся во всплывающем окне.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сенсорный ввод Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 
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
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="aea0d-106">начало работы с сообщениями касания Windows</span><span class="sxs-lookup"><span data-stu-id="aea0d-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="aea0d-107">В этом разделе объясняются задачи, связанные с получением входных данных Windows Touch для работы в приложении.</span><span class="sxs-lookup"><span data-stu-id="aea0d-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="aea0d-108">При работе с сообщениями Windows Touch обычно выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="aea0d-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="aea0d-109">Проверьте возможности входного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="aea0d-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="aea0d-110">Зарегистрируйтесь для получения сообщений Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="aea0d-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="aea0d-111">Обработайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea0d-111">Handle the messages.</span></span>

<span data-ttu-id="aea0d-112">Для Windows Touch используется сообщение [**WM \_ Touch**](wm-touchdown.md).</span><span class="sxs-lookup"><span data-stu-id="aea0d-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="aea0d-113">Это сообщение указывает различные состояния контакта с дигитайзером.</span><span class="sxs-lookup"><span data-stu-id="aea0d-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="aea0d-114">Тестирование возможностей входного дигитайзера</span><span class="sxs-lookup"><span data-stu-id="aea0d-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="aea0d-115">Функцию [жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) можно использовать для запроса возможностей входного дигитайзера путем передачи значения *ниндекс* в **SM \_ дигитайзере**.</span><span class="sxs-lookup"><span data-stu-id="aea0d-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="aea0d-116">[Жетсистемметрикс](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) возвращает битовое поле, которое указывает, готово ли устройство, поддерживает ли устройство перо или сенсорный ввод, является ли устройство ввода интегрированным или внешним, а также поддерживает ли устройство несколько входов (Windows Touch).</span><span class="sxs-lookup"><span data-stu-id="aea0d-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="aea0d-117">В следующей таблице показаны биты для различных полей.</span><span class="sxs-lookup"><span data-stu-id="aea0d-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="aea0d-118">bit</span><span class="sxs-lookup"><span data-stu-id="aea0d-118">Bit</span></span>   | <span data-ttu-id="aea0d-119">8</span><span class="sxs-lookup"><span data-stu-id="aea0d-119">8</span></span>           | <span data-ttu-id="aea0d-120">7</span><span class="sxs-lookup"><span data-stu-id="aea0d-120">7</span></span>           | <span data-ttu-id="aea0d-121">6</span><span class="sxs-lookup"><span data-stu-id="aea0d-121">6</span></span>        | <span data-ttu-id="aea0d-122">5</span><span class="sxs-lookup"><span data-stu-id="aea0d-122">5</span></span>        | <span data-ttu-id="aea0d-123">4</span><span class="sxs-lookup"><span data-stu-id="aea0d-123">4</span></span>            | <span data-ttu-id="aea0d-124">3</span><span class="sxs-lookup"><span data-stu-id="aea0d-124">3</span></span>              | <span data-ttu-id="aea0d-125">2</span><span class="sxs-lookup"><span data-stu-id="aea0d-125">2</span></span>              | <span data-ttu-id="aea0d-126">1</span><span class="sxs-lookup"><span data-stu-id="aea0d-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="aea0d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="aea0d-127">Value</span></span> | <span data-ttu-id="aea0d-128">Стек готов</span><span class="sxs-lookup"><span data-stu-id="aea0d-128">Stack Ready</span></span> | <span data-ttu-id="aea0d-129">Множественный ввод</span><span class="sxs-lookup"><span data-stu-id="aea0d-129">Multi-input</span></span> | <span data-ttu-id="aea0d-130">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="aea0d-130">Reserved</span></span> | <span data-ttu-id="aea0d-131">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="aea0d-131">Reserved</span></span> | <span data-ttu-id="aea0d-132">Внешнее перо</span><span class="sxs-lookup"><span data-stu-id="aea0d-132">External Pen</span></span> | <span data-ttu-id="aea0d-133">Интегрированное перо</span><span class="sxs-lookup"><span data-stu-id="aea0d-133">Integrated Pen</span></span> | <span data-ttu-id="aea0d-134">Внешнее касание</span><span class="sxs-lookup"><span data-stu-id="aea0d-134">External Touch</span></span> | <span data-ttu-id="aea0d-135">Интегрированное касание</span><span class="sxs-lookup"><span data-stu-id="aea0d-135">Integrated Touch</span></span> |



 

<span data-ttu-id="aea0d-136">Чтобы проверить результат команды для определенной функции, можно использовать побитовый оператор & и определенный бит, который тестируется.</span><span class="sxs-lookup"><span data-stu-id="aea0d-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="aea0d-137">Например, чтобы протестировать Windows Touch, необходимо проверить, установлен ли бит седьмого порядка (0x40 в шестнадцатеричном формате).</span><span class="sxs-lookup"><span data-stu-id="aea0d-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="aea0d-138">В следующем примере кода показано, как можно проверить эти значения.</span><span class="sxs-lookup"><span data-stu-id="aea0d-138">The following code example shows how these values could be tested.</span></span>


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



<span data-ttu-id="aea0d-139">В следующей таблице перечислены константы, определенные в Windows. h для тестирования сенсорных возможностей входного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="aea0d-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="aea0d-140">Имя</span><span class="sxs-lookup"><span data-stu-id="aea0d-140">Name</span></span>                   | <span data-ttu-id="aea0d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="aea0d-141">Value</span></span>      | <span data-ttu-id="aea0d-142">Описание</span><span class="sxs-lookup"><span data-stu-id="aea0d-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aea0d-143">Конфигурация ПЛАНШЕТа \_ \_ нет</span><span class="sxs-lookup"><span data-stu-id="aea0d-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="aea0d-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aea0d-144">0x00000000</span></span> | <span data-ttu-id="aea0d-145">У входного дигитайзера нет возможностей сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="aea0d-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="aea0d-146">\_интегрированное \_ КАСАНИе NID</span><span class="sxs-lookup"><span data-stu-id="aea0d-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="aea0d-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aea0d-147">0x00000001</span></span> | <span data-ttu-id="aea0d-148">Для ввода используется интегрированный сенсорный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="aea0d-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="aea0d-149">NID \_ внешнее \_ касание</span><span class="sxs-lookup"><span data-stu-id="aea0d-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="aea0d-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="aea0d-150">0x00000002</span></span> | <span data-ttu-id="aea0d-151">Для ввода используется внешний сенсорный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="aea0d-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="aea0d-152">\_интегрированное \_ перо NID</span><span class="sxs-lookup"><span data-stu-id="aea0d-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="aea0d-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="aea0d-153">0x00000004</span></span> | <span data-ttu-id="aea0d-154">Для ввода используется интегрированный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="aea0d-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="aea0d-155">\_внешнее \_ перо NID</span><span class="sxs-lookup"><span data-stu-id="aea0d-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="aea0d-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="aea0d-156">0x00000008</span></span> | <span data-ttu-id="aea0d-157">Для ввода используется внешний дигитайзер пера.</span><span class="sxs-lookup"><span data-stu-id="aea0d-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="aea0d-158">NID \_ Multi \_ input</span><span class="sxs-lookup"><span data-stu-id="aea0d-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="aea0d-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="aea0d-159">0x00000040</span></span> | <span data-ttu-id="aea0d-160">Для входных данных используется входной дигитайзер с поддержкой нескольких входов.</span><span class="sxs-lookup"><span data-stu-id="aea0d-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="aea0d-161">NID \_ Готово</span><span class="sxs-lookup"><span data-stu-id="aea0d-161">NID\_READY</span></span>             | <span data-ttu-id="aea0d-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="aea0d-162">0x00000080</span></span> | <span data-ttu-id="aea0d-163">Входной дигитайзер готов для ввода.</span><span class="sxs-lookup"><span data-stu-id="aea0d-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="aea0d-164">Если это значение не задано, это может означать, что служба планшета остановлена, дигитайзер не поддерживается или драйверы дигитайзера не установлены.</span><span class="sxs-lookup"><span data-stu-id="aea0d-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="aea0d-165">Проверка значений NID \_ \* является удобным способом проверки возможностей компьютера пользователя, чтобы настроить приложение для использования сенсорного ввода, пера или не планшета.</span><span class="sxs-lookup"><span data-stu-id="aea0d-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="aea0d-166">Например, если у вас есть динамический пользовательский интерфейс (UI) и вы хотите автоматически настроить некоторые из них, можно проверить \_ встроенное \_ касание NID, NID \_ Мультисенсорная и получить максимальное число касаний при первом запуске приложения пользователем.</span><span class="sxs-lookup"><span data-stu-id="aea0d-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="aea0d-167">Существуют некоторые ограничения для SM \_ жетсистемметрикс.</span><span class="sxs-lookup"><span data-stu-id="aea0d-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="aea0d-168">Например, Plug and Play не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aea0d-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="aea0d-169">По этой причине следует соблюдать осторожность при использовании этой функции в качестве средства для постоянной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="aea0d-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="aea0d-170">Регистрация для получения сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="aea0d-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="aea0d-171">Перед получением сенсорного ввода Windows сначала приложения должны зарегистрироваться для получения сенсорного ввода Windows.</span><span class="sxs-lookup"><span data-stu-id="aea0d-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="aea0d-172">Зарегистрировав окно приложения, приложение указывает, что оно совместимо с касанием.</span><span class="sxs-lookup"><span data-stu-id="aea0d-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="aea0d-173">После того как приложение регистрирует свое окно, уведомления из драйвера Windows Touch пересылаются в приложение при вводе данных в окне.</span><span class="sxs-lookup"><span data-stu-id="aea0d-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="aea0d-174">Когда приложение завершает работу, оно отменяет регистрацию своего окна для отключения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="aea0d-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="aea0d-175">[**WM \_ СЕНСОРные**](wm-touchdown.md) сообщения в настоящее время являются «жадными».</span><span class="sxs-lookup"><span data-stu-id="aea0d-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="aea0d-176">После получения первого сообщения Touch в окне все сенсорные сообщения отправляются в это окно, пока фокус не будет получен другим окном.</span><span class="sxs-lookup"><span data-stu-id="aea0d-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="aea0d-177">По умолчанию вы получаете [**сообщения \_ жестов WM**](wm-gesture.md) вместо сообщений [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="aea0d-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="aea0d-178">При вызове [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)вы перестанете получать **сообщения \_ жестов WM** .</span><span class="sxs-lookup"><span data-stu-id="aea0d-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="aea0d-179">В следующем коде показано, как приложение может зарегистрироваться для получения сообщений Windows Touch в приложении Win32.</span><span class="sxs-lookup"><span data-stu-id="aea0d-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="aea0d-180">Обработка сообщений касания Windows</span><span class="sxs-lookup"><span data-stu-id="aea0d-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="aea0d-181">Вы можете управлять сообщениями Windows Touch из приложений в операционных системах Windows различными способами.</span><span class="sxs-lookup"><span data-stu-id="aea0d-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="aea0d-182">При программировании приложения с графическим интерфейсом вы добавляете в `WndProc` функцию код, который обрабатывает интересующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea0d-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="aea0d-183">При программировании Microsoft Foundation Class (MFC) или управляемого приложения вы добавляете обработчики для интересующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="aea0d-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="aea0d-184">В следующем примере кода показано, как можно обрабатывать сенсорные сообщения из WndProc в приложении на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="aea0d-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


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





<span data-ttu-id="aea0d-185">В следующем коде показано, как можно реализовать схему сообщений и обработчик сообщений.</span><span class="sxs-lookup"><span data-stu-id="aea0d-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="aea0d-186">Обратите внимание, что сообщения должны быть объявлены в схеме сообщений, а затем должен быть реализован обработчик для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea0d-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="aea0d-187">Например, в приложении MFC это можно объявить в коде диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="aea0d-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="aea0d-188">Обратите внимание, что `OnInitDialog` функция для диалогового окна должна содержать вызов [**регистертаучвиндов**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , например `RegisterTouchWindow(m_hWnd, 0)` .</span><span class="sxs-lookup"><span data-stu-id="aea0d-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


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



<span data-ttu-id="aea0d-189">Прикосновение к окну означает, что они появятся во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="aea0d-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea0d-190">См. также</span><span class="sxs-lookup"><span data-stu-id="aea0d-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea0d-191">Сенсорный ввод Windows</span><span class="sxs-lookup"><span data-stu-id="aea0d-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 
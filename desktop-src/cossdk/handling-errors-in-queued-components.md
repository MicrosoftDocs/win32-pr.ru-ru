---
description: Иногда возникает ситуация, когда сообщение не может быть успешно доставлено в предполагаемое место назначения, обычно из-за проблемы с системой или конфигурацией.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Обработка ошибок в компонентах в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539056"
---
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="75988-103">Обработка ошибок в компонентах в очереди</span><span class="sxs-lookup"><span data-stu-id="75988-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="75988-104">Иногда возникает ситуация, когда сообщение не может быть успешно доставлено в предполагаемое место назначения, обычно из-за проблемы с системой или конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="75988-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="75988-105">Например, сообщение может быть направлено в очередь, которая не существует или может не находиться в состоянии для получения.</span><span class="sxs-lookup"><span data-stu-id="75988-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="75988-106">Программа перемещения сообщений — это средство, которое перемещает все сообщения об ошибках [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) из одной очереди в другую, чтобы их можно было повторить.</span><span class="sxs-lookup"><span data-stu-id="75988-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="75988-107">Программа перемещения сообщений — это объект автоматизации, который можно вызывать с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="75988-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="75988-108">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="75988-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="75988-109">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="75988-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="75988-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="75988-110">Visual Basic</span></span>

<span data-ttu-id="75988-111">В следующем примере кода показано, как создать объект Мессажемовер, задать необходимые свойства и инициировать перемещение.</span><span class="sxs-lookup"><span data-stu-id="75988-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="75988-112">Чтобы использовать его из Visual Basic, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="75988-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="75988-113">Чтобы использовать объект Мессажемовер, на компьютере должна быть установлена служба очереди сообщений, а в приложении, указанном в AppName, должна быть включена поддержка очередей.</span><span class="sxs-lookup"><span data-stu-id="75988-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="75988-114">Сведения об установке очереди сообщений см. в разделе Справка и поддержка в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="75988-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



<span data-ttu-id="75988-115">В следующем Visual Basic коде показано, как вызвать функцию Мимессажемовер.</span><span class="sxs-lookup"><span data-stu-id="75988-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="75988-116">Исходный путь к сообщению является конечной очередью RESTful.</span><span class="sxs-lookup"><span data-stu-id="75988-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="75988-117">Это неиспользуемая очередь, которая является частной очередью очереди сообщений и называется AppName \_ деадкуеуе.</span><span class="sxs-lookup"><span data-stu-id="75988-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="75988-118">Сообщения перемещаются здесь, если транзакция постоянно прерывается при попытке выполнения в пятой очереди повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="75988-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="75988-119">С помощью средства перемещения сообщений можно переместить сообщение обратно в первую очередь, которая называется AppName.</span><span class="sxs-lookup"><span data-stu-id="75988-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="75988-120">Дополнительные сведения об очередях повторных попыток см. в разделе [ошибки на стороне сервера](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="75988-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="75988-121">Если атрибуты очереди разрешены, то перемещение сообщений перемещается в перемещаемое состояние, поэтому сообщения не теряются или дублируются в случае сбоя во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="75988-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="75988-122">Средство сохраняет все свойства сообщения, которые могут быть сохранены при перемещении сообщений из одной очереди в другую.</span><span class="sxs-lookup"><span data-stu-id="75988-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="75988-123">Если сообщения создаются при вызове очередей компонентов COM+, служебная программа перемещения сообщений сохраняет идентификатор безопасности исходного вызывающего объекта при перемещении сообщений между очередями.</span><span class="sxs-lookup"><span data-stu-id="75988-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="75988-124">Если как Целевая, так и исходная очереди являются транзакционными, вся операция выполняется в переходном виде.</span><span class="sxs-lookup"><span data-stu-id="75988-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="75988-125">Если либо исходная, либо очередь назначения не являются транзакционными, операция не выполняется в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="75988-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="75988-126">Непредвиденный сбой (например, сбой) и перезапуск нетранзакционного перемещения могут дублировать перемещаемое сообщение во время сбоя.</span><span class="sxs-lookup"><span data-stu-id="75988-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="75988-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="75988-127">C/C++</span></span>

<span data-ttu-id="75988-128">В следующем примере кода показано, как создать объект Мессажемовер, задать необходимые свойства и инициировать перемещение.</span><span class="sxs-lookup"><span data-stu-id="75988-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="75988-129">Метод ErrorDescription описан в разделе [Интерпретация кодов ошибок](interpreting-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="75988-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="75988-130">Чтобы использовать объект Мессажемовер, на компьютере должна быть установлена служба очереди сообщений, а в приложении, указанном в AppName, должна быть включена поддержка очередей.</span><span class="sxs-lookup"><span data-stu-id="75988-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="75988-131">Сведения об установке очереди сообщений см. в разделе Справка и поддержка в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="75988-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



<span data-ttu-id="75988-132">В следующем коде C++ показано, как вызвать функцию Мимессажемовер.</span><span class="sxs-lookup"><span data-stu-id="75988-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



<span data-ttu-id="75988-133">Исходный путь к сообщению является конечной очередью RESTful.</span><span class="sxs-lookup"><span data-stu-id="75988-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="75988-134">Это неиспользуемая очередь, которая является частной очередью очереди сообщений и называется AppName \_ деадкуеуе.</span><span class="sxs-lookup"><span data-stu-id="75988-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="75988-135">Сообщения перемещаются здесь, если транзакция постоянно прерывается при попытке выполнения в пятой очереди повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="75988-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="75988-136">С помощью средства перемещения сообщений можно переместить сообщение обратно в первую очередь, которая называется AppName.</span><span class="sxs-lookup"><span data-stu-id="75988-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="75988-137">Дополнительные сведения об очередях повторных попыток см. в разделе [ошибки на стороне сервера](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="75988-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="75988-138">Если атрибуты очереди разрешены, то перемещение сообщений перемещается в перемещаемое состояние, поэтому сообщения не теряются или дублируются в случае сбоя во время перемещения.</span><span class="sxs-lookup"><span data-stu-id="75988-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="75988-139">Средство сохраняет все свойства сообщения, которые могут быть сохранены при перемещении сообщений из одной очереди в другую.</span><span class="sxs-lookup"><span data-stu-id="75988-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="75988-140">Если сообщения создаются при вызове очередей компонентов COM+, служебная программа перемещения сообщений сохраняет идентификатор безопасности исходного вызывающего объекта при перемещении сообщений между очередями.</span><span class="sxs-lookup"><span data-stu-id="75988-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="75988-141">Если как Целевая, так и исходная очереди являются транзакционными, вся операция выполняется в переходном виде.</span><span class="sxs-lookup"><span data-stu-id="75988-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="75988-142">Если либо исходная, либо очередь назначения не являются транзакционными, операция не выполняется в рамках транзакции.</span><span class="sxs-lookup"><span data-stu-id="75988-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="75988-143">Непредвиденный сбой (например, сбой) и перезапуск нетранзакционного перемещения могут дублировать перемещаемое сообщение во время сбоя.</span><span class="sxs-lookup"><span data-stu-id="75988-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="75988-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="75988-144">Remarks</span></span>

<span data-ttu-id="75988-145">COM+ обрабатывает прерывания на стороне сервера (Player), перемещая сообщение, которое завершается с ошибкой, на другую «окончательную» очередь, чтобы извлечь его из пути.</span><span class="sxs-lookup"><span data-stu-id="75988-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="75988-146">Прослушиватель и проигрыватель не могут непрерывно перебирать сообщения, которые прерываются.</span><span class="sxs-lookup"><span data-stu-id="75988-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="75988-147">Во многих случаях прерванную транзакцию можно исправить, выполнив действия на сервере.</span><span class="sxs-lookup"><span data-stu-id="75988-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75988-148">См. также</span><span class="sxs-lookup"><span data-stu-id="75988-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75988-149">Ошибки компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="75988-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 




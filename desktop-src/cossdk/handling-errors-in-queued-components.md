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
# <a name="handling-errors-in-queued-components"></a>Обработка ошибок в компонентах в очереди

Иногда возникает ситуация, когда сообщение не может быть успешно доставлено в предполагаемое место назначения, обычно из-за проблемы с системой или конфигурацией. Например, сообщение может быть направлено в очередь, которая не существует или может не находиться в состоянии для получения. Программа перемещения сообщений — это средство, которое перемещает все сообщения об ошибках [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) из одной очереди в другую, чтобы их можно было повторить. Программа перемещения сообщений — это объект автоматизации, который можно вызывать с помощью VBScript.

## <a name="components-services-administrative-tool"></a>Средство администрирования служб компонентов

Не применяется.

## <a name="visual-basic"></a>Visual Basic

В следующем примере кода показано, как создать объект Мессажемовер, задать необходимые свойства и инициировать перемещение. Чтобы использовать его из Visual Basic, добавьте ссылку на библиотеку типов служб COM+.

> [!Note]  
> Чтобы использовать объект Мессажемовер, на компьютере должна быть установлена служба очереди сообщений, а в приложении, указанном в AppName, должна быть включена поддержка очередей. Сведения об установке очереди сообщений см. в разделе Справка и поддержка в меню " **Пуск** ".

 


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



В следующем Visual Basic коде показано, как вызвать функцию Мимессажемовер.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Исходный путь к сообщению является конечной очередью RESTful. Это неиспользуемая очередь, которая является частной очередью очереди сообщений и называется AppName \_ деадкуеуе. Сообщения перемещаются здесь, если транзакция постоянно прерывается при попытке выполнения в пятой очереди повторных попыток. С помощью средства перемещения сообщений можно переместить сообщение обратно в первую очередь, которая называется AppName. Дополнительные сведения об очередях повторных попыток см. в разделе [ошибки на стороне сервера](server-side-errors.md).

Если атрибуты очереди разрешены, то перемещение сообщений перемещается в перемещаемое состояние, поэтому сообщения не теряются или дублируются в случае сбоя во время перемещения. Средство сохраняет все свойства сообщения, которые могут быть сохранены при перемещении сообщений из одной очереди в другую.

Если сообщения создаются при вызове очередей компонентов COM+, служебная программа перемещения сообщений сохраняет идентификатор безопасности исходного вызывающего объекта при перемещении сообщений между очередями. Если как Целевая, так и исходная очереди являются транзакционными, вся операция выполняется в переходном виде. Если либо исходная, либо очередь назначения не являются транзакционными, операция не выполняется в рамках транзакции. Непредвиденный сбой (например, сбой) и перезапуск нетранзакционного перемещения могут дублировать перемещаемое сообщение во время сбоя.

## <a name="cc"></a>C/C++

В следующем примере кода показано, как создать объект Мессажемовер, задать необходимые свойства и инициировать перемещение. Метод ErrorDescription описан в разделе [Интерпретация кодов ошибок](interpreting-error-codes.md).

> [!Note]  
> Чтобы использовать объект Мессажемовер, на компьютере должна быть установлена служба очереди сообщений, а в приложении, указанном в AppName, должна быть включена поддержка очередей. Сведения об установке очереди сообщений см. в разделе Справка и поддержка в меню " **Пуск** ".

 


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



В следующем коде C++ показано, как вызвать функцию Мимессажемовер.


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



Исходный путь к сообщению является конечной очередью RESTful. Это неиспользуемая очередь, которая является частной очередью очереди сообщений и называется AppName \_ деадкуеуе. Сообщения перемещаются здесь, если транзакция постоянно прерывается при попытке выполнения в пятой очереди повторных попыток. С помощью средства перемещения сообщений можно переместить сообщение обратно в первую очередь, которая называется AppName. Дополнительные сведения об очередях повторных попыток см. в разделе [ошибки на стороне сервера](server-side-errors.md).

Если атрибуты очереди разрешены, то перемещение сообщений перемещается в перемещаемое состояние, поэтому сообщения не теряются или дублируются в случае сбоя во время перемещения. Средство сохраняет все свойства сообщения, которые могут быть сохранены при перемещении сообщений из одной очереди в другую.

Если сообщения создаются при вызове очередей компонентов COM+, служебная программа перемещения сообщений сохраняет идентификатор безопасности исходного вызывающего объекта при перемещении сообщений между очередями. Если как Целевая, так и исходная очереди являются транзакционными, вся операция выполняется в переходном виде. Если либо исходная, либо очередь назначения не являются транзакционными, операция не выполняется в рамках транзакции. Непредвиденный сбой (например, сбой) и перезапуск нетранзакционного перемещения могут дублировать перемещаемое сообщение во время сбоя.

## <a name="remarks"></a>Комментарии

COM+ обрабатывает прерывания на стороне сервера (Player), перемещая сообщение, которое завершается с ошибкой, на другую «окончательную» очередь, чтобы извлечь его из пути. Прослушиватель и проигрыватель не могут непрерывно перебирать сообщения, которые прерываются. Во многих случаях прерванную транзакцию можно исправить, выполнив действия на сервере.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ошибки компонентов в очереди](queued-components-errors.md)
</dt> </dl>

 

 




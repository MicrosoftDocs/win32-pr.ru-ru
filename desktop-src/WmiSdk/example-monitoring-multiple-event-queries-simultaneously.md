---
description: В следующем примере скрипта показано Асинхронное уведомление о событии, использующее метод SWbemServices.ExeКнотификатионкуерясинк и объект Свбемсинк.
ms.assetid: 8beb9804-088e-4dd1-adc8-a29ca450a220
ms.tgt_platform: multiple
title: Пример. одновременное отслеживание нескольких запросов событий
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d70aff849cce81d6628b80f39e57a7f2430af056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702666"
---
# <a name="example-monitoring-multiple-event-queries-simultaneously"></a><span data-ttu-id="78362-103">Пример. одновременное отслеживание нескольких запросов событий</span><span class="sxs-lookup"><span data-stu-id="78362-103">Example: Monitoring Multiple Event Queries Simultaneously</span></span>

<span data-ttu-id="78362-104">В следующем примере скрипта показано Асинхронное уведомление о событии, использующее метод [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md) и объект [**свбемсинк**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="78362-104">The following script example shows asynchronous event notification, making use of the [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) method and [**SWbemSink**](swbemsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="78362-105">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="78362-105">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="78362-106">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="78362-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 


```VB
Dim WithEvents sink As SWbemSink

Private Sub ExecNoteAsync_Click()

    Dim services As SWbemServices
    Dim strQuery As String
    Dim cntxt As SWbemNamedValueSet
    Set sink = New SWbemSink
    Set services = GetObject( _
        "winmgmts:{impersonationLevel=impersonate,(security)}")
    strQuery = "SELECT * FROM __InstanceCreationEvent "& _
                "WHERE TargetInstance ISA 'Win32_NTLogEvent'"
    Set cntxt = New SWbemNamedValueSet
    cntxt.Add "sinkname", "ExecNoteAsync"
    services.Security_.Privileges.Add (wbemPrivilegeSecurity)
    services.ExecNotificationQueryAsync sink, strQuery, , , , cntxt
    MsgBox "This program will asynchronously " _
        & "process Win32_NTLogEvent events."
        
End Sub

Private Sub sink_OnObjectReady( _
             ByVal objWbemObject As WbemScripting.ISWbemObject, 
             ByVal objWbemAsyncContext As _
                 WbemScripting.ISWbemNamedValueSet)
  On Error GoTo ErrorHandler
    Dim cntxt_item As WbemScripting.SWbemNamedValue

    Set cntxt_item = objWbemAsyncContext.Item("sinkname")
        
    If cntxt_item.Value = "ExecNoteAsync" Then
        MsgBox " Got event: " & objWbemObject.TargetInstance.Message
    End If

    Set objWbemObject = Nothing

    Exit Sub                                   ' Exit to avoid handler

ErrorHandler:
    MsgBox "Error number: " & Str(Err.Number) & vbNewLine & _
    "Description: " & Err.Description, vbCritical
End Sub
```



 

 




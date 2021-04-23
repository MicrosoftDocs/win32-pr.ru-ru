---
title: Перехват ошибок в ADSI
description: VBScript предлагает только один способ перехвата ошибок во встроенной обработке ошибок.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654131"
---
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="985c8-103">Перехват ошибок в ADSI</span><span class="sxs-lookup"><span data-stu-id="985c8-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="985c8-104">VBScript предлагает только один способ перехвата ошибок: встроенная обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="985c8-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="985c8-105">Встроенный обработчик ошибок начинается с оператора **On Error Resume Next** .</span><span class="sxs-lookup"><span data-stu-id="985c8-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="985c8-106">С момента **возобновления ошибки Next** предотвратит остановку выполнения скрипта до конца области, из которой вызывается **Error Resume Next** , необходимо проверить значение **Err** в каждой точке после оператора **On Error Resume Next** , где может возникнуть ошибка.</span><span class="sxs-lookup"><span data-stu-id="985c8-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="985c8-107">В следующем примере демонстрируется встроенная обработка ошибок в скрипте ADSI:</span><span class="sxs-lookup"><span data-stu-id="985c8-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



<span data-ttu-id="985c8-108">После каждого расположения, в котором сценарий может столкнуться с ошибкой, существует оператор **If Err** .</span><span class="sxs-lookup"><span data-stu-id="985c8-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="985c8-109">Объект **Err** содержит код ошибки последней ошибки, произошедшей во время выполнения скрипта. Если ошибка не возникла, то **Err** всегда будет равняться нулю (0).</span><span class="sxs-lookup"><span data-stu-id="985c8-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="985c8-110">В предыдущем примере ошибка приведет к выполнению перехода к подпрограмме **адсиерр** , которая проверяет значение **Err. Number** для ожидаемых ошибок.</span><span class="sxs-lookup"><span data-stu-id="985c8-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="985c8-111">Вместо умирающие с незашифрованным сообщением об ошибке сценарий даст несколько лучшего объяснения о том, почему оно остановлено.</span><span class="sxs-lookup"><span data-stu-id="985c8-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="985c8-112">Помните, что в области, в которой вызывается **Error Resume Next** , любая ошибка, возникающая после **следующего вызова On Error Resume** , будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="985c8-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="985c8-113">Это может усложнить отладку сценария, если вы забыли проверить значение **Err** в соответствующих местах.</span><span class="sxs-lookup"><span data-stu-id="985c8-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="985c8-114">В любом месте, где возникает ошибка, обязательно проверьте значение **Err**.</span><span class="sxs-lookup"><span data-stu-id="985c8-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="985c8-115">(При первоначальной отладке скрипта можно просто позволить сценарию остановить его выполнение и отобразить ошибочный номер строки при ошибке, а затем добавить обработчики ошибок после того, как основная последовательность программы будет правильна.)</span><span class="sxs-lookup"><span data-stu-id="985c8-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 





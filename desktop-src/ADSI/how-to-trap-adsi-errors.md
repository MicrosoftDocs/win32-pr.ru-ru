---
title: Перехват ошибок в ADSI
description: VBScript предлагает только один способ перехвата ошибок во встроенной обработке ошибок.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082538"
---
# <a name="how-to-trap-adsi-errors"></a>Перехват ошибок в ADSI

VBScript предлагает только один способ перехвата ошибок: встроенная обработка ошибок. Встроенный обработчик ошибок начинается с оператора **On Error Resume Next** . С момента **возобновления ошибки Next** предотвратит остановку выполнения скрипта до конца области, из которой вызывается **Error Resume Next** , необходимо проверить значение **Err** в каждой точке после оператора **On Error Resume Next** , где может возникнуть ошибка. В следующем примере демонстрируется встроенная обработка ошибок в скрипте ADSI:


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



После каждого расположения, в котором сценарий может столкнуться с ошибкой, существует оператор **If Err** . Объект **Err** содержит код ошибки последней ошибки, произошедшей во время выполнения скрипта. Если ошибка не возникла, то **Err** всегда будет равняться нулю (0). В предыдущем примере ошибка приведет к выполнению перехода к подпрограмме **адсиерр** , которая проверяет значение **Err. Number** для ожидаемых ошибок. Вместо умирающие с незашифрованным сообщением об ошибке сценарий даст несколько лучшего объяснения о том, почему оно остановлено.

Помните, что в области, в которой вызывается **Error Resume Next** , любая ошибка, возникающая после **следующего вызова On Error Resume** , будет пропущена. Это может усложнить отладку сценария, если вы забыли проверить значение **Err** в соответствующих местах. В любом месте, где возникает ошибка, обязательно проверьте значение **Err**.

(При первоначальной отладке скрипта можно просто позволить сценарию остановить его выполнение и отобразить ошибочный номер строки при ошибке, а затем добавить обработчики ошибок после того, как основная последовательность программы будет правильна.)

 

 





---
description: Выполнение асинхронного вызова метода WMI или метода поставщика позволяет скрипту продолжать выполнение, пока объекты возвращают в объект Свбемсинк и обрабатываются такими методами, как Свбемсинк. Онобжектреади.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Выполнение асинхронного вызова с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702298"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Выполнение асинхронного вызова с помощью VBScript

Выполнение асинхронного вызова [*метода WMI*](gloss-w.md) или [*метода поставщика*](gloss-p.md) позволяет скрипту продолжать выполнение, пока объекты возвращают в объект [**свбемсинк**](swbemsink.md) и обрабатываются такими методами, как [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md). Однако асинхронные вызовы не рекомендуются, так как данные могут не возвращаться на том же уровне безопасности, что и вызов метода.

При использовании асинхронных вызовов приемника, таких как [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) , для получения возвращаемых данных можно задать следующее значение реестра.

**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **унсекаппакцессконтролдефаулт**

Установка этого значения реестра гарантирует проверку подлинности объектов данных, возвращаемых в приемник. Если для **унсекаппакцессконтролдефаулт** задано значение One (1), WMI выполняет проверку доступа к возвращаемым данным. Проверки доступа проверяют, поступают ли данные из правильного источника. Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

Асинхронные методы с именами, заканчивающимися на "Async \_ ", всегда возвращают немедленно после вызова, чтобы программа могла продолжить выполнение. Например, [**SWbemServices.Exeккуери**](swbemservices-execquery.md) является синхронным и блокирует выполнение до тех пор, пока не будут возвращены все объекты. [**SWbemServices.Exeметод ккуерясинк**](swbemservices-execqueryasync.md) является неблокирующей асинхронной версией. Более безопасный способ вызоваSWbemServices.Exeнеблокировке **ккуери** заключается в вызове [*полусинхронном*](gloss-s.md). Дополнительные сведения см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md) и [вызов Семисинчронаус с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).

Параметр *ифлагс* для асинхронных вызовов всегда имеет значение по умолчанию (0). Асинхронные методы не предоставляют коллекцию [**SWbemObjectSet**](swbemobjectset.md) для подпрограммы приемника. Вместо этого подпрограммы события [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) в скрипте или приложении получают каждый объект, как он предоставляется.

После завершения исходного асинхронного вызова он вызывает событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в приемнике объекта и выполняет код, который вы поместите в него, чтобы обработать результат вызова.

> [!Note]  
> Страница Active Server (ASP) в качестве сервера скриптов не поддерживает асинхронный вызов.

 

Следующая процедура описывает, как выполнить асинхронный вызов с помощью VBScript.

**Выполнение асинхронного вызова с помощью VBScript**

1.  Подключитесь к инструментарию WMI и получите объект [**SwbemServices**](swbemservices.md) .

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Создайте приемник объекта с помощью функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) или (для сервера скриптов Windows 2,0) тег объекта с атрибутом Events, имеющим значение **true**.

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -или-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Создайте подпрограммы для каждого события, которое может быть активировано асинхронным событием. Эти события определяются как методы в [**SWbemObject**](swbemobject.md). Например, Инструментарий WMI выполняет обратный вызов к [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) по мере того, как каждый экземпляр возвращает.

    При создании подпрограммы разместите код в подпрограмме, чтобы обрабатывались все события при его получении.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Изучите параметр *ихресулт* , возвращаемый [**oncompleteed**](swbemsink-oncompleted.md) , чтобы определить, завершился ли асинхронный вызов успешно, или если произошла ошибка. В случае успеха значение, передаваемое в параметре *ихресулт* , равно нулю (0). Любое другое значение может указывать на ошибку, поэтому следует проверить значения в объекте Error, возвращенном в параметре *обжерроробжект* .

4.  Выполните асинхронный вызов и передайте имя приемника в параметр *обжвбемсинк* .

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Выполните вызов, который предотвращает завершение скрипта до получения всех событий. Если сценарий может работать с интерфейсом экрана, простой способ сделать это — использовать команду сервера сценариев Windows (WSH) `Echo` , которая показана в следующем примере.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    При выполнении этого скрипта может отобразиться первый экземпляр, возвращаемый перед сообщением **ожидания экземпляров** , либо он появится после. Это характер асинхронной обработки. Если закрыть окно сообщения **Waiting of Instances (ожидание экземпляров** ), возможно, вы не увидите все экземпляры.

6.  Если имеются результаты из нескольких различных асинхронных вызовов, возвращающих один и тот же приемник, сохраните все необходимые отличительные данные в параметре контекста *обжвбемасинкконтекст* .

7.  По завершении работы с приемником отмените асинхронный вызов с помощью метода [**Cancel**](swbemsink-cancel.md) .

    ```VB
    objwbemsink.Cancel()
    ```

    

    Метод [**Cancel**](swbemsink-cancel.md) предписывает WSH отменить все асинхронные вызовы, связанные с данным объектом-приемником. Таким образом, может потребоваться использовать отдельные приемники для асинхронных операций, которые должны быть независимыми.

8.  Освободите объект приемника, назначив объекту приемника значение `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

В следующем примере кода показан асинхронный запрос для всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) на локальном компьютере. Сведения о семисинчронаус версии того же метода см. в разделе [вызов метода](calling-a-method.md).


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 

---
description: Инструментарий WMI предоставляет методы в API COM и API сценариев для получения информации или работы с объектами в корпоративной системе.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Вызов метода WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6c8a74c8125e0bb1727839b8f59f4b486161d5ae629a0c7351481ade016ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820091"
---
# <a name="calling-a-wmi-method"></a>Вызов метода WMI

Инструментарий WMI предоставляет методы в [API COM](com-api-for-wmi.md) и [API сценариев](scripting-api-for-wmi.md) для получения информации или работы с объектами в корпоративной системе. Например, метод создания сценариев WMI [**SWbemServices.Exeккуери**](swbemservices-execquery.md) запросы данных. Поставщики также имеют методы, определенные в регистрируемых ими классах. Примерами являются [**методы \_ Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) и [**счедулеауточк**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) , предоставляемые [поставщиком Win32](/windows/desktop/CIMWin32Prov/win32-provider).

В этом разделе обсуждаются следующие разделы:

-   [Методы WMI по сравнению с методами поставщика](#wmi-methods-compared-to-provider-methods)
-   [Режимы вызова методов в WMI](#method-calling-modes-in-wmi)
    -   [Синхронный режим](#synchronous-mode)
    -   [Асинхронный режим](#asynchronous-mode)
    -   [Режим семисинчронаус](#semisynchronous-mode)
-   [Связанные темы](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Методы WMI по сравнению с методами поставщика

Используя вызовы [*методов WMI*](gloss-w.md) , Объединенные с вызовами [*методов поставщика*](gloss-p.md) , можно получать сведения о предприятии и управлять ими. Дополнительные сведения см. [в разделе вызов метода WMI](calling-a-wmi-method.md) и [вызов метода поставщика](calling-a-provider-method.md).

Методы объекта сценариев WMI [**SWbemObject**](swbemobject.md) имеют особое состояние, так как они могут применяться к любому классу данных WMI. Дополнительные сведения см. в разделе [Создание скриптов с помощью SWbemObject](scripting-with-swbemobject.md).

В следующем примере кода вызываются методы WMI и provider.

Следующие методы WMI и поставщика находятся в [API скриптов для WMI](scripting-api-for-wmi.md):

-   **objWMIService.Exeккуери** вызывает метод создания сценариев WMI [ **SWbemServices.Exeккуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **обжсервице. No ()** вызывает метод поставщика [ **Win32 \_ Service.**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Вы можете найти код, который может появиться в разделе "return" раздела "коды возврата" для [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Режимы Method-Calling в WMI

Режим вызова семисинчронаус обычно обеспечивает оптимальный баланс между безопасностью и производительностью.

Дополнительные сведения о каждом из возможных режимов см. в следующих статьях:

-   [Синхронная](#synchronous-mode)
-   [Асинхронный](#asynchronous-mode)
-   [семисинчронаус](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Синхронный режим

Синхронный режим происходит, когда программа или скрипты приостанавливаются до тех пор, пока вызов метода не вернет объект коллекции [**SWbemObjectSet**](swbemobjectset.md) . Инструментарий WMI создает эту коллекцию в памяти перед возвратом объекта коллекции вызывающей программе или сценарию.

Синхронный режим может оказать негативное воздействие на производительность программы или сценария на компьютере, на котором запущена программа или сценарий. Например, синхронное извлечение тысяч событий из журнала событий может занять много времени и использовать большой объем памяти, так как инструментарий WMI создает объект из каждого события и затем помещает эти объекты в коллекцию перед передачей коллекции в метод.

Вызывать методы, которые не возвращают большие наборы данных, следует только в синхронном режиме. В синхронном режиме можно безопасно вызывать следующие методы [**SwbemServices**](swbemservices.md) :

-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExeКмесод**](swbemservices-execmethod.md)
-   [**SWbemServices. Get**](swbemservices-get.md)

Любые методы [**SwbemServices**](swbemservices.md) без слова «Async» в имени могут вызываться в синхронном режиме путем установки значения **вбемфлагретурнвхенкомплете** в параметре *ифлагс* .

### <a name="asynchronous-mode"></a>Асинхронный режим

Асинхронный режим происходит, когда программа или скрипт продолжит выполняться после вызова метода. Инструментарий WMI возвращает все объекты из метода в объект [**свбемсинк**](swbemsink.md) при создании каждого объекта. Вызывающая программа или скрипт должны иметь объект **свбемсинк** и обработчик событий [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) для обработки возвращаемых объектов. Дополнительные сведения о создании обработчика событий для асинхронного режима см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).

Хотя в этом режиме нет потерь производительности и ресурсов в синхронном режиме, асинхронный режим может привести к серьезным угрозам безопасности, поскольку результаты, хранящиеся в объекте [**свбемсинк**](swbemsink.md) , могут не поступать из вызывающей программы или скрипта. Инструментарий WMI понижает уровень проверки подлинности объекта **свбемсинк** до тех пор, пока метод не завершится. Дополнительные сведения об устранении этих угроз безопасности см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

Методы, добавленные с помощью слова async, являются методами для асинхронного режима. Следующие методы являются асинхронными вызовами:

-   [**SWbemServices. АссоЦиаторсофасинк**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExeКмесодасинк**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExeКнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExeКкуерясинк**](swbemservices-execqueryasync.md)
-   [**SWbemServices. Инстанцесофасинк**](swbemservices-instancesofasync.md)
-   [**SWbemServices. Референцестоасинк**](swbemservices-referencesto.md)
-   [**SWbemServices. Субклассесофасинк**](swbemservices-subclassesofasync.md)

Дополнительные сведения об асинхронном режиме см. в следующих статьях:

-   [Создание асинхронного вызова с помощью C++](making-an-asynchronous-call-with-c--.md)
-   [Выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Режим семисинчронаус

Режим семисинчронаус аналогичен асинхронному режиму в том, что программа или скрипт продолжит выполняться после вызова метода. В режиме семисинчронаус Инструментарий WMI получает объекты в фоновом режиме по мере продолжения выполнения скрипта или программы. Инструментарий WMI возвращает каждый объект, возвращаемый вызывающему методу сразу после создания объекта.

Так как инструментарий WMI управляет объектом, режим семисинчронаус более безопасен, чем асинхронный режим. Однако если используется режим семисинчронаус с более чем 1 000 экземплярами, то извлечение экземпляра может захватить доступные ресурсы, что может привести к снижению производительности программы или сценария, а также от компьютера, использующего программу или сценарий. Каждый объект берет необходимые ресурсы, пока память не будет освобождена.

Чтобы обойти это условие, можно вызвать метод с набором параметров *ифлагс* с флагами **вбемфлагфорвардонли** и **вбемфлагретурниммедиатели** , чтобы дать инструментарию WMI инструкцию вернуть [**SWbemObjectSet**](swbemobjectset.md)только в прямом направлении. Однонаправленная **SWbemObjectSet** устраняет проблему производительности, вызванную большим набором данных, освобождая память после перечисления объекта.

Любой метод [**SwbemServices**](swbemservices.md) , который не может быть вызван в синхронном или асинхронном режиме, вызывается в режиме семисинчронаус.

В режиме семисинчронаус вызываются следующие методы:

-   [**SWbemServices. АссоЦиаторсоф**](swbemservices-associatorsof.md)
-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExeКмесод**](swbemservices-execmethod.md)
-   [**SWbemServices.ExeКнотификатионкуери**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExeКкуери**](swbemservices-execquery.md)
-   [**SWbemServices. Get**](swbemservices-get.md)
-   [**SWbemServices. Инстанцесоф**](swbemservices-instancesof.md)
-   [**SWbemServices. Референцесто**](swbemservices-referencesto.md)
-   [**SWbemServices. Субклассесоф**](swbemservices-subclassesof.md)
-   [**SWbemServices. размещение**](swbemservicesex-put.md)

Дополнительные сведения о режиме семисинчронаус см. в статьях [осуществление вызова семисинчронаус с помощью C++](making-a-semisynchronous-call-with-c--.md) и [выполнение семисинчронаус Call с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Повышение производительности перечисления](improving-enumeration-performance.md)
</dt> <dt>

[Создание сценариев с помощью SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**вбемфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 

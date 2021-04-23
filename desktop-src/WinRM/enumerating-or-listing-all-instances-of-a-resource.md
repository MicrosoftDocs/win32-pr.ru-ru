---
title: Перечисление или составление списка всех экземпляров ресурса
description: Метод Session. Enumerate является служба удаленного управления Windowsным подходом для получения всех экземпляров указанного ресурса.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260962"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="c03fe-103">Перечисление или составление списка всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="c03fe-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="c03fe-104">Метод [**Session. Enumerate**](session-enumerate.md) является служба удаленного управления Windowsным подходом для получения всех экземпляров указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="c03fe-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="c03fe-105">Метод [**Session. Enumerate**](session-enumerate.md) не получает коллекцию в объекте [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) , например [**SWbemService.ExeКкуери**](/windows/desktop/WmiSdk/swbemservices-execquery) Call с [запросом WMI](/windows/desktop/WmiSdk/querying-wmi) в качестве параметра (например, `ExecQuery("SELECT * from Win32_LogicalDisk")` ), или вызов метода, например [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="c03fe-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="c03fe-106">Метод **Session. Enumerate** и объект [**перечислителя**](enumerator.md) гораздо более похож на операцию объекта [TextStream](/previous-versions//312a5kbt(v=vs.85)) скриптов, который используется для чтения файлов в виде потока.</span><span class="sxs-lookup"><span data-stu-id="c03fe-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="c03fe-107">Чтобы считать файлы в виде текстового потока, необходимо создать объект скрипта [TextStream](/previous-versions//312a5kbt(v=vs.85)) и вызвать метод [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) для чтения каждой строки файла.</span><span class="sxs-lookup"><span data-stu-id="c03fe-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="c03fe-108">Аналогичным образом можно вызвать метод [**Session. Enumerate**](session-enumerate.md) , чтобы получить объект [**перечислителя**](enumerator.md) и вызвать метод [**Enumerator. ReadItem**](enumerator-readitem.md) для получения следующего элемента.</span><span class="sxs-lookup"><span data-stu-id="c03fe-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="c03fe-109">Как и при чтении из текстового файла, можно вызвать свойство [**Enumerator. атендофстреам**](enumerator-atendofstream.md) , чтобы проверить, достигли ли вы конца элементов данных.</span><span class="sxs-lookup"><span data-stu-id="c03fe-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="c03fe-110">**Перечисление ресурсов**</span><span class="sxs-lookup"><span data-stu-id="c03fe-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="c03fe-111">Создание сеанса.</span><span class="sxs-lookup"><span data-stu-id="c03fe-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="c03fe-112">Создайте универсальный код ресурса (URI) для обнаружения ресурса.</span><span class="sxs-lookup"><span data-stu-id="c03fe-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="c03fe-113">Вызовите метод [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="c03fe-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="c03fe-114">Этот вызов запускает перечисление.</span><span class="sxs-lookup"><span data-stu-id="c03fe-114">This call starts an enumeration.</span></span> <span data-ttu-id="c03fe-115">В WinRM операция перечисления не получает коллекцию точно так же, как это делает WMI.</span><span class="sxs-lookup"><span data-stu-id="c03fe-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="c03fe-116">Вместо этого метод **Session. Enumerate** устанавливает WS-Management контекст перечисления протокола, который поддерживается в объекте [**перечислителя**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="c03fe-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="c03fe-117">Вызовите метод [**Enumerator. ReadItem**](enumerator-readitem.md) , чтобы получить следующий элемент результатов.</span><span class="sxs-lookup"><span data-stu-id="c03fe-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="c03fe-118">В WS-Management Protocol это соответствует операции извлечения.</span><span class="sxs-lookup"><span data-stu-id="c03fe-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="c03fe-119">Используйте метод [**Enumerator. атендофстреам**](enumerator-atendofstream.md) в качестве элемента управления, чтобы выяснить, когда следует прерывать чтение.</span><span class="sxs-lookup"><span data-stu-id="c03fe-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="c03fe-120">В следующем примере кода VBScript показан полный скрипт.</span><span class="sxs-lookup"><span data-stu-id="c03fe-120">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="c03fe-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c03fe-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c03fe-122">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="c03fe-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c03fe-123">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="c03fe-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c03fe-124">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="c03fe-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 
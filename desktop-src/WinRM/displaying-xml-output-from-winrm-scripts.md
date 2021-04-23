---
title: Отображение выходных данных XML из скриптов WinRM
description: Служба удаленного управления Windows скрипты возвращают XML, а не объекты. Формат XML не предназначен для восприятия. Для преобразования данных в удобочитаемый формат можно использовать методы API MSXML и предварительно установленный XSL-файл.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070397"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="95407-105">Отображение выходных данных XML из скриптов WinRM</span><span class="sxs-lookup"><span data-stu-id="95407-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="95407-106">Служба удаленного управления Windows скрипты возвращают XML, а не объекты.</span><span class="sxs-lookup"><span data-stu-id="95407-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="95407-107">Формат XML не предназначен для восприятия.</span><span class="sxs-lookup"><span data-stu-id="95407-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="95407-108">Для преобразования данных в удобочитаемый формат можно использовать методы API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) и предварительно установленный XSL-файл.</span><span class="sxs-lookup"><span data-stu-id="95407-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="95407-109">Дополнительные сведения об XML-выходных данных и примерах XML в формате RAW см. [в разделе сценарии в Служба удаленного управления Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="95407-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="95407-110">Программа командной строки **WinRM** поставляется с файлом преобразования с именем всмткст. xsl, который отображает выходные данные в табличной форме.</span><span class="sxs-lookup"><span data-stu-id="95407-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="95407-111">Если скрипт передает этот файл методам MSXML, выполняющим преобразует данные, выходные данные отображаются так же, как и выходные данные средства **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="95407-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="95407-112">**Форматирование необработанных выходных данных XML**</span><span class="sxs-lookup"><span data-stu-id="95407-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="95407-113">Создайте объект [**WSMan**](wsman.md) и создайте сеанс.</span><span class="sxs-lookup"><span data-stu-id="95407-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="95407-114">Создание объектов MSXML, представляющих выходные данные XML-ответа и преобразования XSL.</span><span class="sxs-lookup"><span data-stu-id="95407-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="95407-115">Получение данных с помощью методов объекта [**сеанса**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="95407-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="95407-116">Укажите ответ на метод MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) и метод [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) для хранения файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="95407-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="95407-117">Используйте метод [TRANSFORMNODE](/previous-versions/windows/desktop/ms761399(v=vs.85)) MSXML и отобразите или сохраните выходные данные.</span><span class="sxs-lookup"><span data-stu-id="95407-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="95407-118">В следующем примере кода VBScript показан полный скрипт.</span><span class="sxs-lookup"><span data-stu-id="95407-118">The following VBScript code example shows the complete script.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="95407-119">Добавление переносимой подпрограммы для преобразования XML в скрипты</span><span class="sxs-lookup"><span data-stu-id="95407-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="95407-120">Можно добавить подпрограммы в скрипты, использующие предустановленный XSL-файл для преобразования необработанных выходных данных из скрипта WinRM в табличную форму.</span><span class="sxs-lookup"><span data-stu-id="95407-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="95407-121">Следующая подпрограммы использует вызовы методов создания скриптов MSXML для предоставления выходных данных в Всмткст. xsl.</span><span class="sxs-lookup"><span data-stu-id="95407-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



<span data-ttu-id="95407-122">Следующая подпрограммы преобразует каждую строку данных, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="95407-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## <a name="related-topics"></a><span data-ttu-id="95407-123">См. также</span><span class="sxs-lookup"><span data-stu-id="95407-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95407-124">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="95407-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="95407-125">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="95407-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="95407-126">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="95407-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 
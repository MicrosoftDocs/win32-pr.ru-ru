---
description: Библиотеку типов сценариев WMI можно использовать для вызова методов API сценариев WMI из Microsoft Visual Studio и в файлах Windows Script, WSF-файлов.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Использование библиотеки типов сценариев WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702652"
---
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="ab88d-103">Использование библиотеки типов сценариев WMI</span><span class="sxs-lookup"><span data-stu-id="ab88d-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="ab88d-104">Библиотеку типов сценариев WMI можно использовать для вызова методов API сценариев WMI из Microsoft Visual Studio и в файлах Windows Script, WSF-файлов.</span><span class="sxs-lookup"><span data-stu-id="ab88d-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="ab88d-105">Использование библиотеки типов сценариев WMI с Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ab88d-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="ab88d-106">Компоненты Visual InterDev 6,0 интегрированы в [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab88d-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="ab88d-107">В следующей процедуре описывается, как включить в интегрированной среде разработки (IDE) сведения о библиотеке типов Вбемскриптинг.</span><span class="sxs-lookup"><span data-stu-id="ab88d-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="ab88d-108">**Добавление библиотеки типов сценариев WMI в ссылки проекта**</span><span class="sxs-lookup"><span data-stu-id="ab88d-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="ab88d-109">В меню **проект** выберите команду **Добавить ссылки** .</span><span class="sxs-lookup"><span data-stu-id="ab88d-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="ab88d-110">На вкладке COM в поле **Добавить ссылку** выберите БИБЛИОТЕКУ Microsoft WMI Scripting v 1.2.</span><span class="sxs-lookup"><span data-stu-id="ab88d-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="ab88d-111">Если в списке ссылки нет соответствующего параметра, добавьте его с помощью **кнопки Обзор** в поле **ссылки** .</span><span class="sxs-lookup"><span data-stu-id="ab88d-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="ab88d-112">На странице **Обзор** открывается поле **Добавить ссылку** , позволяющее найти библиотеку типов вбемскриптинг.</span><span class="sxs-lookup"><span data-stu-id="ab88d-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="ab88d-113">Библиотека типов Вбемскриптинг находится в файле Wbemdisp. tlb в каталоге% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="ab88d-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="ab88d-114">Выберите файл и нажмите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="ab88d-114">Select the file and click **Open**.</span></span> <span data-ttu-id="ab88d-115">Библиотека Microsoft WMI Scripting V 1.2 отображается в списке ссылок.</span><span class="sxs-lookup"><span data-stu-id="ab88d-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="ab88d-116">Убедитесь, что в списке рядом с этим элементом выбрано поле.</span><span class="sxs-lookup"><span data-stu-id="ab88d-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="ab88d-117">Использование библиотеки типов сценариев WMI с сервером сценариев Windows 2,0</span><span class="sxs-lookup"><span data-stu-id="ab88d-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="ab88d-118">Можно включить ссылку на **вбемскриптинг. SWbemLocator** в файл WSF сервера сценариев Windows, в отличие от скрипта, написанного на Visual Basic, Scripting Edition или других языках сценариев.</span><span class="sxs-lookup"><span data-stu-id="ab88d-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="ab88d-119">Это позволяет использовать вместо значений константные имена.</span><span class="sxs-lookup"><span data-stu-id="ab88d-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="ab88d-120">Например, при настройке проверки подлинности используйте **вбемаусентикатионлевелпктприваци** вместо значения 6.</span><span class="sxs-lookup"><span data-stu-id="ab88d-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="ab88d-121">Сценарии могут подключаться с помощью API скриптов для библиотеки типов WMI, используя следующие методы:</span><span class="sxs-lookup"><span data-stu-id="ab88d-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="ab88d-122">Указание идентификатора GUID Вбемскриптинг в методах VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) и [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="ab88d-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="ab88d-123">Это оповещает сервер сценариев Windows о подключении к набору объектов WMI.</span><span class="sxs-lookup"><span data-stu-id="ab88d-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="ab88d-124">В следующем примере кода VBScript создается новый объект [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="ab88d-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="ab88d-125">Использование [строки моникера](constructing-a-moniker-string.md) "винмгмтс:" при получении нового или существующего объекта.</span><span class="sxs-lookup"><span data-stu-id="ab88d-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="ab88d-126">В следующем примере кода VBScript используется моникер "винмгмтс:" для получения экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) со свойством **Handle** , равным 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="ab88d-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="ab88d-127">**Handle** — это ключевое свойство для этого класса.</span><span class="sxs-lookup"><span data-stu-id="ab88d-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="ab88d-128">Ссылка на библиотеку типов WMI с помощью <reference> тега формата XML-файла WSH 2,0.</span><span class="sxs-lookup"><span data-stu-id="ab88d-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="ab88d-129">При использовании <reference> тега тег должен иметь либо атрибут **UUID** , значение которого является **идентификатором GUID** библиотеки типов WMI, либо (рекомендуется) атрибут объекта, значение которого является **идентификатором ProgID** любого из объектов сценариев WMI, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="ab88d-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="ab88d-130">В следующем примере кода VBScript используется идентификатор PROGID "Вбемскриптинг".</span><span class="sxs-lookup"><span data-stu-id="ab88d-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="ab88d-131">Чтобы выполнить сценарий, сохраните текст в файл с расширением. wsf.</span><span class="sxs-lookup"><span data-stu-id="ab88d-131">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   <span data-ttu-id="ab88d-132">Использование <**объекта**> тега для создания объекта скрипта WMI.</span><span class="sxs-lookup"><span data-stu-id="ab88d-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="ab88d-133">Можно указать атрибут **ID** со значением имени, которое ссылается на создаваемый объект скрипта WMI, и атрибут **ProgID** , равный проид объекта сценариев WMI.</span><span class="sxs-lookup"><span data-stu-id="ab88d-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="ab88d-134">Следующий сценарий WSH отображает имя узла и количество процессоров на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab88d-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="ab88d-135">Чтобы выполнить сценарий, сохраните текст в файл с расширением. wsf.</span><span class="sxs-lookup"><span data-stu-id="ab88d-135">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ab88d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ab88d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab88d-137">Создание сценариев в WMI</span><span class="sxs-lookup"><span data-stu-id="ab88d-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="ab88d-138">API сценариев для инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="ab88d-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 

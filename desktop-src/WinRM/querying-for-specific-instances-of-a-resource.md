---
title: Запрос конкретных экземпляров ресурса
description: Вызов Session. Enumerate имеет необязательные параметры, которые позволяют уменьшить перечисление в запрос.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700869"
---
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="01a28-103">Запрос конкретных экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="01a28-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="01a28-104">Вызов [**Session. Enumerate**](session-enumerate.md) имеет необязательные параметры, которые позволяют уменьшить перечисление в запрос.</span><span class="sxs-lookup"><span data-stu-id="01a28-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="01a28-105">Так как [API-интерфейсы WinRM](winrm-scripting-api.md) и [API для WinRM](winrm-c---api.md) в тесно моделируются по базовому протоколу WS-Management, параметры используют одну и ту же терминологию для запросов в качестве *диалекта* протокола —*фильтра* и фильтра.</span><span class="sxs-lookup"><span data-stu-id="01a28-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="01a28-106">Можно использовать параметры Filter и диалекта [**Session. Enumerate**](session-enumerate.md) , либо можно создать и предоставить объект [**ResourceLocator**](resourcelocator.md) и метод [**аддселектор**](resourcelocator-addselector.md) , но нельзя выполнить оба действия.</span><span class="sxs-lookup"><span data-stu-id="01a28-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="01a28-107">Эта процедура выполняет запрос для сетевых адаптеров, которые привязаны к TCP/IP и включены.</span><span class="sxs-lookup"><span data-stu-id="01a28-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="01a28-108">Запрос запрашивает все экземпляры [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) , для которых свойство **IpEnabled** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="01a28-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="01a28-109">За исключением добавления *фильтра* и *диалекта*, запрос обрабатывается как простое перечисление.</span><span class="sxs-lookup"><span data-stu-id="01a28-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="01a28-110">В этом примере имя ресурса для константы ресурса представлено звездочкой " \* ", поскольку имя класса [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)уже упоминается в строке *стрфилтер* .</span><span class="sxs-lookup"><span data-stu-id="01a28-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="01a28-111">**Запрос конкретных экземпляров ресурса**</span><span class="sxs-lookup"><span data-stu-id="01a28-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="01a28-112">Для простоты чтения определите URI как константы.</span><span class="sxs-lookup"><span data-stu-id="01a28-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="01a28-113">Создание сеанса.</span><span class="sxs-lookup"><span data-stu-id="01a28-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="01a28-114">Создайте строку фильтра.</span><span class="sxs-lookup"><span data-stu-id="01a28-114">Construct the filter string.</span></span> <span data-ttu-id="01a28-115">Служба удаленного управления Windows поддерживает [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) в качестве диалекта фильтра.</span><span class="sxs-lookup"><span data-stu-id="01a28-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="01a28-116">Задайте необходимые [**константы перечисления**](enumeration-constants.md) в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="01a28-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="01a28-117">Имейте в виду, что если флаги включают в себя [**константы перечисления**](enumeration-constants.md) **всманфлагхиерарчидипбасепропсонли** или **всманфлагхиерарчишаллов** , служба WinRM возвращает код ошибки **Error, \_ \_ \_ \_ не поддерживаемый режимом полиморфизма WSMan**.</span><span class="sxs-lookup"><span data-stu-id="01a28-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="01a28-118">Вызовите метод [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="01a28-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="01a28-119">Этот вызов запускает перечисление.</span><span class="sxs-lookup"><span data-stu-id="01a28-119">This call starts an enumeration.</span></span> <span data-ttu-id="01a28-120">Метод **Session. Enumerate** устанавливает WS-Management контекст перечисления протокола, который сохраняется в объекте [**перечислителя**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="01a28-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="01a28-121">Вызовите метод [**Enumerator. ReadItem**](enumerator-readitem.md) , чтобы получить следующий элемент результатов.</span><span class="sxs-lookup"><span data-stu-id="01a28-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="01a28-122">В WS-Management Protocol это соответствует операции извлечения.</span><span class="sxs-lookup"><span data-stu-id="01a28-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="01a28-123">Используйте метод [**Enumerator. атендофстреам**](enumerator-atendofstream.md) в качестве элемента управления, чтобы выяснить, когда следует прерывать чтение.</span><span class="sxs-lookup"><span data-stu-id="01a28-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="01a28-124">В следующем примере кода VBScript показан полный скрипт.</span><span class="sxs-lookup"><span data-stu-id="01a28-124">The following VBScript code example shows the complete script.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="01a28-125">См. также</span><span class="sxs-lookup"><span data-stu-id="01a28-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a28-126">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="01a28-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01a28-127">Перечисление или вывод всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="01a28-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="01a28-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="01a28-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 
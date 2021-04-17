---
description: Описывает создание страниц Microsoft Active Server Pages (ASP), отображающих сведения об удаленных компьютерах на компьютерах, на которых не установлен инструментарий WMI.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Создание страниц Active Server для WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703314"
---
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="00a01-103">Создание страниц Active Server для WMI</span><span class="sxs-lookup"><span data-stu-id="00a01-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="00a01-104">Microsoft Active Server Pages (ASP) позволяет создавать динамические веб-страницы, включая сценарии на стороне сервера и на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="00a01-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="00a01-105">Страницы ASP могут работать гораздо быстрее, чем клиентские HTML-страницы, так как большая часть работы выполняется на сервере.</span><span class="sxs-lookup"><span data-stu-id="00a01-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="00a01-106">Страницы ASP также можно использовать для вывода сведений о удаленных компьютерах на других компьютерах, на которых не установлен инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="00a01-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="00a01-107">В следующей процедуре описывается использование инструментария WMI с ASP.</span><span class="sxs-lookup"><span data-stu-id="00a01-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="00a01-108">**Использование инструментария WMI с ASP**</span><span class="sxs-lookup"><span data-stu-id="00a01-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="00a01-109">Напишите страницу ASP, использующую WMI, и поместите ее в каталог, доступный для веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="00a01-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="00a01-110">Сценарии ASP для WMI можно разработать с помощью нескольких языков сценариев, включая VBScript.</span><span class="sxs-lookup"><span data-stu-id="00a01-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="00a01-111">Можно создать часть скрипта WMI страницы ASP точно так же, как при создании любого другого сценария, использующего WMI, с одним важным ограничением: нельзя использовать асинхронные методы WMI в страницах ASP.</span><span class="sxs-lookup"><span data-stu-id="00a01-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="00a01-112">Обратите внимание, что любые вызовы **GetObject** или **CreateObject** должны находиться в коде на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="00a01-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="00a01-113">Дополнительные сведения см. в разделе [API скриптов для инструментария WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="00a01-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="00a01-114">Настройка конфигурации проверки подлинности для службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="00a01-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="00a01-115">Дополнительные сведения см. в разделе [Настройка IIS 5 и более поздних версий для сценариев ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="00a01-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="00a01-116">Отключите анонимный доступ и включите встроенную проверку подлинности Windows для файла ASP.</span><span class="sxs-lookup"><span data-stu-id="00a01-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="00a01-117">Эти параметры для страницы ASP можно настроить с помощью оснастки IIS, расположенной в папке **Администрирование** **панели управления**.</span><span class="sxs-lookup"><span data-stu-id="00a01-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="00a01-118">Пример ASP-страницы WMI</span><span class="sxs-lookup"><span data-stu-id="00a01-118">WMI ASP Page Example</span></span>

<span data-ttu-id="00a01-119">В следующем примере используется инструментарий управления Windows (WMI) (WMI) в Active Server странице (ASP) для вывода IP-адреса и параметров шлюза IP по умолчанию для сервера, на котором выполняется этот сценарий.</span><span class="sxs-lookup"><span data-stu-id="00a01-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 




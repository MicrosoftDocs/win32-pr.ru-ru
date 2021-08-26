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
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030614"
---
# <a name="creating-active-server-pages-for-wmi"></a>Создание страниц Active Server для WMI

Microsoft Active Server Pages (ASP) позволяет создавать динамические веб-страницы, включая сценарии на стороне сервера и на стороне клиента. Страницы ASP могут работать гораздо быстрее, чем клиентские HTML-страницы, так как большая часть работы выполняется на сервере. страницы ASP также можно использовать для вывода сведений о удаленных компьютерах на других компьютерах, на которых не установлен инструментарий управления Windows (WMI) (WMI).

В следующей процедуре описывается использование инструментария WMI с ASP.

**Использование инструментария WMI с ASP**

1.  Напишите страницу ASP, использующую WMI, и поместите ее в каталог, доступный для веб-сервера.

    Сценарии ASP для WMI можно разработать с помощью нескольких языков сценариев, включая VBScript. Можно создать часть скрипта WMI страницы ASP точно так же, как при создании любого другого сценария, использующего WMI, с одним важным ограничением: нельзя использовать асинхронные методы WMI в страницах ASP. Обратите внимание, что любые вызовы **GetObject** или **CreateObject** должны находиться в коде на стороне сервера. Дополнительные сведения см. в разделе [API скриптов для инструментария WMI](scripting-api-for-wmi.md).

2.  настройка конфигурации проверки подлинности для службы IIS (IIS). Дополнительные сведения см. в разделе [Настройка IIS 5 и более поздних версий для сценариев ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).
3.  отключите анонимный доступ и включите встроенную проверку подлинности Windows для файла ASP. Эти параметры для страницы ASP можно настроить с помощью оснастки IIS, расположенной в папке **Администрирование** **панели управления**.

## <a name="wmi-asp-page-example"></a>Пример ASP-страницы WMI

в следующем примере используется инструментарий управления Windows (WMI) (WMI) в Active Server странице (ASP) для вывода IP-адреса и параметров шлюза ip по умолчанию для сервера, на котором выполняется этот сценарий.


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



 

 




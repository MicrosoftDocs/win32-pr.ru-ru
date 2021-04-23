---
title: начало работы с ASP для ADSI
description: Интерфейсы ADSI можно использовать для доступа к данным каталога с помощью страницы ASP. Это может быть удобным способом выполнения задач администрирования и запросов с веб-страницы или предоставления сведений сотрудникам в интрасети.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ASP ADSI
- ADSI, страницы ASP
- ADSI, страницы ASP, пример кода ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772956"
---
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="1e5bf-107">начало работы с ASP для ADSI</span><span class="sxs-lookup"><span data-stu-id="1e5bf-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="1e5bf-108">Интерфейсы ADSI можно использовать для доступа к данным каталога с помощью страницы ASP.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="1e5bf-109">Это может быть удобным способом выполнения задач администрирования и запросов с веб-страницы или предоставления сведений сотрудникам в интрасети.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="1e5bf-110">Одним из преимуществ использования ADSI с ASP является то, что вы можете создавать более широкие возможности для пользователей, поскольку вы можете использовать Visual Basic, чтобы создать приложение ADSI и предложить его пользователю через стандартную веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="1e5bf-111">Например, можно создать веб-страницу, которая позволяет сотрудникам ввести фамилию сотрудника и возвратить номер телефона для этого сотрудника, или создать форму, позволяющую сотрудникам обновлять персональные данные в базе данных отдела кадров компании.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="1e5bf-112">Код ASP начинается с "<%" и заканчивается на "% >".</span><span class="sxs-lookup"><span data-stu-id="1e5bf-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="1e5bf-113">Можно добавить код ADSI в качестве VBScript или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="1e5bf-114">Чтобы создать страницу ASP, можно воспользоваться редактором веб-страниц, блокнотом или другим текстовым редактором или системой разработки Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="1e5bf-115">Перед запуском страницы ASP настройте приложение или сервер IIS в соответствии с инструкциями в статье [проблемы проверки подлинности для ADSI с ASP](authentication-issues-for-adsi-with-asp.md).</span><span class="sxs-lookup"><span data-stu-id="1e5bf-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="1e5bf-116">Простой пример ASP: перечисление объектов в контейнере</span><span class="sxs-lookup"><span data-stu-id="1e5bf-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="1e5bf-117">С помощью редактора веб-страниц создайте новую HTML-страницу, которая принимает различающееся имя объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="1e5bf-118">Введите следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-118">Enter the following code example.</span></span>


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



<span data-ttu-id="1e5bf-119">Теперь эта страница может принять имя контейнера, которое ему передается, и использовать ADSI для перечисления объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="1e5bf-120">Создайте новую ASP-страницу с именем Enum. ASP и введите следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="1e5bf-121">Сохраните эту страницу в корне локального веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="1e5bf-121">Save this page at the root of the local web server.</span></span>


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 





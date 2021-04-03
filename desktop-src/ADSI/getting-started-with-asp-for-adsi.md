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
# <a name="getting-started-with-asp-for-adsi"></a>начало работы с ASP для ADSI

Интерфейсы ADSI можно использовать для доступа к данным каталога с помощью страницы ASP. Это может быть удобным способом выполнения задач администрирования и запросов с веб-страницы или предоставления сведений сотрудникам в интрасети.

Одним из преимуществ использования ADSI с ASP является то, что вы можете создавать более широкие возможности для пользователей, поскольку вы можете использовать Visual Basic, чтобы создать приложение ADSI и предложить его пользователю через стандартную веб-страницу. Например, можно создать веб-страницу, которая позволяет сотрудникам ввести фамилию сотрудника и возвратить номер телефона для этого сотрудника, или создать форму, позволяющую сотрудникам обновлять персональные данные в базе данных отдела кадров компании.

Код ASP начинается с "<%" и заканчивается на "% >". Можно добавить код ADSI в качестве VBScript или Visual Basic.

Чтобы создать страницу ASP, можно воспользоваться редактором веб-страниц, блокнотом или другим текстовым редактором или системой разработки Microsoft Visual Studio .NET.

Перед запуском страницы ASP настройте приложение или сервер IIS в соответствии с инструкциями в статье [проблемы проверки подлинности для ADSI с ASP](authentication-issues-for-adsi-with-asp.md).

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Простой пример ASP: перечисление объектов в контейнере

С помощью редактора веб-страниц создайте новую HTML-страницу, которая принимает различающееся имя объекта контейнера. Введите следующий пример кода.


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



Теперь эта страница может принять имя контейнера, которое ему передается, и использовать ADSI для перечисления объектов в контейнере.

Создайте новую ASP-страницу с именем Enum. ASP и введите следующий пример кода. Сохраните эту страницу в корне локального веб-сервера.


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



 

 





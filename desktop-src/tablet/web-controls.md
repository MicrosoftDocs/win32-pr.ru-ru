---
description: Одним из способов создания веб-приложений с поддержкой рукописного ввода является помещение Windows Forms элементов управления в авебпажевисин Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Веб-элементы управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701447"
---
# <a name="web-controls"></a><span data-ttu-id="c0a8c-103">Веб-элементы управления</span><span class="sxs-lookup"><span data-stu-id="c0a8c-103">Web Controls</span></span>

<span data-ttu-id="c0a8c-104">Одним из способов создания веб-приложений с поддержкой рукописного ввода является помещение Windows Forms элементов управления в авебпажевисин Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="c0a8c-105">Хороший учебник по этому методу можно найти в статье [использование Windows Forms элементов управления в Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0a8c-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="c0a8c-106">Основные шаги в этом учебнике:</span><span class="sxs-lookup"><span data-stu-id="c0a8c-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="c0a8c-107">Создайте элемент управления, наследующий от [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="c0a8c-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="c0a8c-108">Создайте HTML-страницу с тегом объекта, который ссылается на этот UserControl.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="c0a8c-109">Создайте виртуальный каталог и задайте разрешения.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="c0a8c-110">Загрузите URL-адрес HTML-страницы в браузер.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="c0a8c-111">Этот метод можно применить к элементам управления с поддержкой рукописного ввода, как и к любому другому [**элементу управления**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="c0a8c-112">На самом деле, этот метод можно использовать с любым классом в Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="c0a8c-113">Примеры, предоставляемые пакетом средств разработки программного обеспечения (SDK) Microsoft Windows XP Tablet PC Edition, включают версию веб-элемента управления Auto CLAIMS в разделе веб-образцы рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="c0a8c-114">Этот пример принимает исходный [образец автоматической заявки](auto-claims-form-sample.md) и превращает его в элемент управления, помещаемый на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="c0a8c-115">Дополнительные сведения о веб-включении этого образца см. в [примере веб-элемента управления рукописного ввода](ink-web-control-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c0a8c-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="c0a8c-116">При развертывании приложения, созданного с помощью .NET, через Интернет, на приложение может повлиять модель безопасности для .NET.</span><span class="sxs-lookup"><span data-stu-id="c0a8c-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="c0a8c-117">Дополнительные сведения о том, как безопасность работает с веб-приложениями с поддержкой рукописного ввода, см. в разделе [безопасность и доверие](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="c0a8c-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 

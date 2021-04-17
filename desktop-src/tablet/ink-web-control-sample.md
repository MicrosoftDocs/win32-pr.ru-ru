---
description: В этом примере показано, как создать элемент управления с поддержкой рукописного ввода для использования в веб-браузере. Образец принимает исходный образец автоматической заявки и превращает его в элемент управления, помещаемый на веб-страницу.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Пример веб-элемента управления рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710989"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="06da2-104">Пример веб-элемента управления рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="06da2-104">Ink Web Control Sample</span></span>

<span data-ttu-id="06da2-105">В этом примере показано, как создать элемент управления с поддержкой рукописного ввода для использования в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="06da2-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="06da2-106">Образец принимает исходный [образец автоматической заявки](auto-claims-form-sample.md) и превращает его в элемент управления, помещаемый на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="06da2-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="06da2-107">Дополнительные сведения об использовании рукописного ввода в Интернете см. в разделе [Рукописный ввод в Интернете](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="06da2-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="06da2-108">Изменения в исходном образце проекта</span><span class="sxs-lookup"><span data-stu-id="06da2-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="06da2-109">Этот пример состоит из решения, включающего два проекта и HTML-файл.</span><span class="sxs-lookup"><span data-stu-id="06da2-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="06da2-110">Первый проект, Автоутверждение, представляет собой \# проект библиотеки элементов управления Microsoft Visual C (пользовательский элемент управления).</span><span class="sxs-lookup"><span data-stu-id="06da2-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="06da2-111">Исходный код для этого элемента управления практически идентичен образцу автозаявок с двумя отличиями:</span><span class="sxs-lookup"><span data-stu-id="06da2-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="06da2-112">`AutoClaims`Класс в этом примере наследует от класса [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) , а не от класса [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="06da2-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="06da2-113">Класс автозаявок в этом образце содержит добавленный открытый метод, `DisposeResources` удаляющий внутренние дочерние элементы управления, используемые для сбора рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="06da2-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="06da2-114">Этот метод должен вызываться севебпажеон, который используется при завершении страницы с помощью элемента управления.</span><span class="sxs-lookup"><span data-stu-id="06da2-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="06da2-115">Ссылка на элемент управления в HTML</span><span class="sxs-lookup"><span data-stu-id="06da2-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="06da2-116">Решение включает HTML-файл default.htm.</span><span class="sxs-lookup"><span data-stu-id="06da2-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="06da2-117">Этот файл представляет собой страницу, к которой переходит браузер, чтобы загрузить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="06da2-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="06da2-118">Файл содержит <object> тег, который ссылается на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="06da2-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="06da2-119">Он также включает сценарий, который вызывается при выгрузке страницы, как указано в атрибуте OnLoad = " `OnUnload()` " в</span><span class="sxs-lookup"><span data-stu-id="06da2-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="06da2-120">в XML.</span><span class="sxs-lookup"><span data-stu-id="06da2-120">tag.</span></span> <span data-ttu-id="06da2-121">Эта функция вызывает `DisposeResources` метод для элемента управления, чтобы обеспечить правильную отпускания всех ресурсов при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="06da2-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="06da2-122">Обратите внимание на формат значения атрибута ClassID для <object> тега.</span><span class="sxs-lookup"><span data-stu-id="06da2-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="06da2-123">Он именует сборку, за которой следует \# Разделитель знаков, а затем пространство имен, содержащее элемент управления, а затем имя класса элемента управления.</span><span class="sxs-lookup"><span data-stu-id="06da2-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="06da2-124">Реальный пользовательский элемент управления, скорее всего, будет включать дополнительные методы, используемые для сохранения или отправки данных, собираемых в приложении.</span><span class="sxs-lookup"><span data-stu-id="06da2-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="06da2-125">Проект WebControl для автозаявок \_</span><span class="sxs-lookup"><span data-stu-id="06da2-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="06da2-126">Проект WebControl для автозаявок \_ — это проект развертывания, который создает программу установки, которая добавляет виртуальный корневой каталог, автозапрос \_ WebControl на веб-сервере при установке.</span><span class="sxs-lookup"><span data-stu-id="06da2-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="06da2-127">Элемент управления и HTML-файл помещаются в этот виртуальный корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="06da2-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="06da2-128">Скомпилированные веб-образцы не устанавливаются с помощью параметра установки по умолчанию для пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="06da2-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="06da2-129">Необходимо выполнить выборочную установку и выбрать подпараметр "предварительно скомпилированные веб-примеры", чтобы установить их.</span><span class="sxs-lookup"><span data-stu-id="06da2-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06da2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="06da2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06da2-131">Пример формы Auto Claims</span><span class="sxs-lookup"><span data-stu-id="06da2-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="06da2-132">Рукописный ввод в Интернете</span><span class="sxs-lookup"><span data-stu-id="06da2-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 

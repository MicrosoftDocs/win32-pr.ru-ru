---
description: В этом примере показано, как развернуть управляемое приложение для планшетных ПК через Интернет с помощью развертывания без вмешательства пользователя.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Пример веб-примера развертывания No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547282"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="7995f-103">Пример веб-примера развертывания No-Touch</span><span class="sxs-lookup"><span data-stu-id="7995f-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="7995f-104">В этом примере показано, как развернуть управляемое приложение для планшетных ПК через Интернет с помощью развертывания без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="7995f-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="7995f-105">Вы должны быть знакомы с концепциями, обсуждаемыми в разделе [Несенсорное развертывание в платформа .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span><span class="sxs-lookup"><span data-stu-id="7995f-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="7995f-106">Для запуска этого примера на компьютере должен быть установлен Microsoft службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="7995f-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="7995f-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="7995f-107">Overview</span></span>

<span data-ttu-id="7995f-108">Благодаря несенсорному развертыванию приложения для планшетных Пквиндовс Forms — приложения для настольных систем, созданные с помощью классов в пространстве имен System. Windows. Forms платформы Microsoft .NET Framework и Microsoft Windows XP Tablet PC Edition 1,7 — могут быть скачаны, установлены и запущены непосредственно на компьютерах пользователей без изменения реестра или общих системных компонентов.</span><span class="sxs-lookup"><span data-stu-id="7995f-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="7995f-109">Этот пример принимает исходный проект для [образца формы Auto утверждений, автоматическую](auto-claims-form-sample.md)заявку и предоставляет проект установщика с автоутверждением \_ нотаучвеб.</span><span class="sxs-lookup"><span data-stu-id="7995f-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="7995f-110">После компиляции и запуска проект установщика создает новый виртуальный корень, который также называется автозаявками \_ нотаучвеб.</span><span class="sxs-lookup"><span data-stu-id="7995f-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="7995f-111">Программа установки копирует файл default.htm, содержащий ссылку на сборку AutoClaims.exe.</span><span class="sxs-lookup"><span data-stu-id="7995f-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="7995f-112">Чтобы запустить клиентское приложение с богатыми возможностями, перейдите к виртуальному корню с помощью Microsoft Internet Explorer и щелкните ссылку на странице default.htm.</span><span class="sxs-lookup"><span data-stu-id="7995f-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="7995f-113">Для работы приложения в домене приложения Internet Explorer необходимо перейти к виртуальному корню с помощью IIS (например, https://localhost/AutoClaims\_NoTouchWeb/default.htm) а не напрямую через файловую систему).</span><span class="sxs-lookup"><span data-stu-id="7995f-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="7995f-114">Требования к развертыванию No-Touch</span><span class="sxs-lookup"><span data-stu-id="7995f-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="7995f-115">Все зависимые сборки должны находиться либо в пути поиска сборок, либо в корне виртуального каталога веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="7995f-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="7995f-116">Проект развертывания нотаучвеб автоматических утверждений \_ устанавливает сборку и ссылающуюся страницу default.htm в один и тот же виртуальный корень (автоутверждения \_ нотаучвеб).</span><span class="sxs-lookup"><span data-stu-id="7995f-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="7995f-117">Скомпилированные веб-образцы не устанавливаются с помощью параметра установки по умолчанию для пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="7995f-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="7995f-118">Необходимо выполнить выборочную установку и выбрать подпараметр "предварительно скомпилированные веб-примеры", чтобы установить их.</span><span class="sxs-lookup"><span data-stu-id="7995f-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="7995f-119">Дополнительные сведения об использовании рукописного ввода в Интернете см. в разделе [Рукописный ввод в Интернете](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="7995f-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 
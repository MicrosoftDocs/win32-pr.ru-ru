---
description: Создание пакетов установки для приложений COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Создание пакетов установки для приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701210"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="795b0-103">Создание пакетов установки для приложений COM+</span><span class="sxs-lookup"><span data-stu-id="795b0-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="795b0-104">Для создания пакетов установки приложений COM+ и прокси приложений можно использовать средство администрирования служб компонентов или библиотеку администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="795b0-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="795b0-105">COM+ создает установщик Windows пакеты установки, которые в одном файле содержат все необходимые компоненты для установки приложения COM+ на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="795b0-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="795b0-106">При экспорте приложения COM+ средство администрирования служб компонентов определяет набор классов, компонентов и их атрибутов, а также атрибуты уровня приложения.</span><span class="sxs-lookup"><span data-stu-id="795b0-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="795b0-107">На основе этих сведений средство администрирования служб компонентов создает один MSI-файл, который содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="795b0-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="795b0-108">Установщик Windows таблицы со сведениями о регистрации COM (Дополнительные сведения см. в документации по установщик Windows).</span><span class="sxs-lookup"><span data-stu-id="795b0-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="795b0-109">АПЛ файл, содержащий атрибуты приложения.</span><span class="sxs-lookup"><span data-stu-id="795b0-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="795b0-110">(Это внутренний файл; формат этого файла не документирован.)</span><span class="sxs-lookup"><span data-stu-id="795b0-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="795b0-111">Библиотеки DLL и библиотеки типов, описывающие интерфейсы, реализуемые классами приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="795b0-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="795b0-112">В дополнение к MSI-файлу средство администрирования служб компонентов создает CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="795b0-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="795b0-113">Этот файл является оболочкой для MSI-файла, позволяя разработчику развернуть приложение COM+ через Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="795b0-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="795b0-114">При экспорте приложения COM+ пакет средств администрирования служб компонентов упаковывает только стандартные компоненты COM+ приложения.</span><span class="sxs-lookup"><span data-stu-id="795b0-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="795b0-115">Он не упаковывается, например, в зависимую библиотеку DLL или файлы данных.</span><span class="sxs-lookup"><span data-stu-id="795b0-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="795b0-116">Перед установкой приложения COM+ необходимо сначала установить на компьютере зависимые DLL-файлы.</span><span class="sxs-lookup"><span data-stu-id="795b0-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="795b0-117">Кроме того, можно использовать средство разработки установщик Windows, чтобы добавить эти зависимые файлы в MSI файл, созданный средством администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="795b0-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="795b0-118">(Дополнительные сведения см. в документации по установщик Windows.)</span><span class="sxs-lookup"><span data-stu-id="795b0-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="795b0-119">Установка приложений COM+ на других компьютерах</span><span class="sxs-lookup"><span data-stu-id="795b0-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="795b0-120">Файл установщик Windows (. msi), созданный средством администрирования служб компонентов, можно использовать для установки приложения COM+ на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="795b0-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="795b0-121">MSI-файл, содержащий приложение COM+, может быть установлен только на компьютерах, поддерживающих службы COM+.</span><span class="sxs-lookup"><span data-stu-id="795b0-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="795b0-122">Подробные инструкции по развертыванию приложений COM+ см. в разделе «Установка приложений COM+» справки по администрированию служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="795b0-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="795b0-123">Если MSI-файл не изменяется с помощью средства установщик Windows Authoring Tool, то приложения COM+, установленные с помощью установщик Windows, отображаются на панели управления Установка и удаление программ.</span><span class="sxs-lookup"><span data-stu-id="795b0-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="795b0-124">См. также</span><span class="sxs-lookup"><span data-stu-id="795b0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="795b0-125">Развертывание прокси приложения</span><span class="sxs-lookup"><span data-stu-id="795b0-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="795b0-126">Каталог COM+</span><span class="sxs-lookup"><span data-stu-id="795b0-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 




---
description: Узнайте, как использовать средство анализатора Standard User Analyzer (SUA) и мастер SUA для тестирования приложений и обнаружения потенциальных проблем совместимости.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Анализатор доступа учетных записей (SUA) и соответствующий мастер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314587"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="76f35-103">Анализатор доступа учетных записей (SUA) и соответствующий мастер</span><span class="sxs-lookup"><span data-stu-id="76f35-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="76f35-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="76f35-104">Affected Platforms</span></span>

<span data-ttu-id="76f35-105">**Клиенты:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="76f35-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="76f35-106">**Серверы:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76f35-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="76f35-107">Описание</span><span class="sxs-lookup"><span data-stu-id="76f35-107">Description</span></span>

<span data-ttu-id="76f35-108">Набор средств для обеспечения совместимости приложений включает средство анализатора Standard User Analyzer (SUA) и мастер анализатора Standard User Analyzer (мастер SUA).</span><span class="sxs-lookup"><span data-stu-id="76f35-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="76f35-109">Эти средства позволяют тестировать приложения и отслеживать вызовы API для обнаружения потенциальных проблем совместимости из-за функции контроля учетных записей (UAC) в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="76f35-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="76f35-110">Функция UAC, ранее известная как ограниченная учетная запись пользователя (LUA), требует, чтобы все пользователи (включая членов группы администраторов) запускались как обычные пользователи с помощью диалогового окна «запрос безопасности», пока приложение намеренно не потребует повышения прав.</span><span class="sxs-lookup"><span data-stu-id="76f35-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="76f35-111">Однако приложения, которым требуется доступ и привилегии для расположений, недоступных для обычного пользователя, не могут правильно работать со стандартной ролью пользователя.</span><span class="sxs-lookup"><span data-stu-id="76f35-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="76f35-112">Использование</span><span class="sxs-lookup"><span data-stu-id="76f35-112">Usage</span></span>

<span data-ttu-id="76f35-113">В следующих разделах содержатся подробные сведения об использовании средств работы с мастером SUA и SUA.</span><span class="sxs-lookup"><span data-stu-id="76f35-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="76f35-114">**SUA, инструмент**</span><span class="sxs-lookup"><span data-stu-id="76f35-114">**SUA Tool**</span></span>

<span data-ttu-id="76f35-115">Средство SUA позволяет анализировать приложение, просматривать подробный отчет о проблемах, связанных с UAC, а затем применять предлагаемые и выбранные решения по устранению рисков, как показано в следующей блок-схеме.</span><span class="sxs-lookup"><span data-stu-id="76f35-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Схема, на которой показан поток инструментов U.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="76f35-117">*Средство SUA и виртуализация*</span><span class="sxs-lookup"><span data-stu-id="76f35-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="76f35-118">Только средство SUA позволяет включать и отключать функцию виртуализации.</span><span class="sxs-lookup"><span data-stu-id="76f35-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="76f35-119">После отключения функции виртуализации проверенное приложение будет вести себя примерно так, как если бы оно работала в операционной системе Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76f35-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="76f35-120">*Средство SUA и повышенные привилегии*</span><span class="sxs-lookup"><span data-stu-id="76f35-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="76f35-121">Только средство SUA позволяет включать и отключать функцию запуска с **повышенными правами** .</span><span class="sxs-lookup"><span data-stu-id="76f35-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="76f35-122">Функция повышения прав запуска позволяет выбранному приложению запускаться от имени администратора или обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="76f35-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="76f35-123">В зависимости от выбранного варианта вы обнаружите различные типы проблем, связанных с UAC.</span><span class="sxs-lookup"><span data-stu-id="76f35-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="76f35-124">Если снять флажок **запустить с повышенными** правами, приложение будет работать с полными правами администратора, что позволяет SUA прогнозировать проблемы, которые могут возникнуть при работе с обычным пользователем.</span><span class="sxs-lookup"><span data-stu-id="76f35-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="76f35-125">Если установлен флажок Запустить с повышенными правами, то отобразятся ошибки, возникающие в результате фактического выполнения приложения и создания ошибок.</span><span class="sxs-lookup"><span data-stu-id="76f35-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="76f35-126">**Мастер SUA**</span><span class="sxs-lookup"><span data-stu-id="76f35-126">**SUA Wizard**</span></span>

<span data-ttu-id="76f35-127">Мастер SUA позволяет выполнить пошаговый процесс, по которому можно проанализировать приложение, а затем применить предлагаемые и выбранные решения по устранению, как показано в следующей блок-схеме.</span><span class="sxs-lookup"><span data-stu-id="76f35-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="76f35-128">В отличие от средства SUA, мастер не позволяет просматривать подробные сведения о проблемах, связанных с UAC.</span><span class="sxs-lookup"><span data-stu-id="76f35-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Схема, показывающая поток работы мастера S U.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="76f35-130">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="76f35-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="76f35-131">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="76f35-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="76f35-132">[Основные сведения о средствах анализатора Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="76f35-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="76f35-133">[Технический справочник по анализатору Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="76f35-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="76f35-134">[Тестирование и устранение проблем с помощью средств разработки](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="76f35-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="76f35-135">Совместимость приложений и управление учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="76f35-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="76f35-136">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="76f35-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 

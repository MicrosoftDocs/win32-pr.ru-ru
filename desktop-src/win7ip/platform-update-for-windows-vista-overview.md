---
title: Сведения об обновлении платформы для Windows Vista
description: Содержит обзор обновления платформы для Windows Vista и обновления платформы для Windows Server 2008 и их функций.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Обновление платформы для Windows Server 2008
- Обновление платформы для Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105703545"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="27741-105">Сведения об обновлении платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="27741-106">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 — это обновления операционной системы конечных пользователей, которые поддерживают использование выбранных технологий Windows 7 в предыдущих версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="27741-107">Обновления включают набор библиотек времени выполнения, позволяющих разработчикам приложений ориентироваться на текущие выпуски, Windows 7 и Windows Server 2008 R2, а также предыдущие версии, Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="27741-108">Сводка поддерживаемых API по технологиям</span><span class="sxs-lookup"><span data-stu-id="27741-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="27741-109">Каждая технология, поддерживаемая обновлением платформы для Windows Vista и обновления платформы для Windows Server 2008, включает набор API, который можно использовать в приложении, предназначенном для предыдущей версии Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="27741-110">Дополнительные сведения об использовании интерфейсов API, поддерживаемых обновлениями в приложении, предназначенном для предыдущих версий Windows, см. в разделе [Разработка приложения для предыдущих версий Windows](developing-applications-for-previous-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="27741-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="27741-111">Некоторые интерфейсы API, связанные с технологией, могут не поддерживаться, а поведение, производительность или требования некоторых поддерживаемых интерфейсов API могут различаться в разных версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="27741-112">Чтобы получить дополнительные сведения о поддерживаемом API для конкретной технологии, щелкните ссылку в одной из сводных таблиц, чтобы открыть раздел об этой технологии.</span><span class="sxs-lookup"><span data-stu-id="27741-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="27741-113">Технологии, поддерживаемые при обновлении платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="27741-114">Чтобы получить дополнительные сведения о поддерживаемом API для конкретной технологии, щелкните ссылку в одной из сводных таблиц, чтобы открыть раздел об этой технологии.</span><span class="sxs-lookup"><span data-stu-id="27741-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="27741-115">В следующей таблице приведены технологии, поддерживаемые для Windows Vista и Windows XP с обновлением платформы для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27741-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="27741-116">Технология</span><span class="sxs-lookup"><span data-stu-id="27741-116">Technology</span></span>                                                                                    | <span data-ttu-id="27741-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-117">Windows Vista</span></span> | <span data-ttu-id="27741-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27741-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="27741-119">API автоматизации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="27741-120">Да</span><span class="sxs-lookup"><span data-stu-id="27741-120">Yes</span></span>           | <span data-ttu-id="27741-121">Да</span><span class="sxs-lookup"><span data-stu-id="27741-121">Yes</span></span>        |
| [<span data-ttu-id="27741-122">Графическая система Windows, работа с образами и библиотека XPS</span><span class="sxs-lookup"><span data-stu-id="27741-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="27741-123">Да</span><span class="sxs-lookup"><span data-stu-id="27741-123">Yes</span></span>           | <span data-ttu-id="27741-124">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-124">No</span></span>         |
| [<span data-ttu-id="27741-125">Лента Windows и Библиотека диспетчера анимации</span><span class="sxs-lookup"><span data-stu-id="27741-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="27741-126">Да</span><span class="sxs-lookup"><span data-stu-id="27741-126">Yes</span></span>           | <span data-ttu-id="27741-127">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-127">No</span></span>         |
| [<span data-ttu-id="27741-128">Платформа портативных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="27741-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="27741-129">Да</span><span class="sxs-lookup"><span data-stu-id="27741-129">Yes</span></span>           | <span data-ttu-id="27741-130">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="27741-131">Технологии, поддерживаемые при обновлении платформы для Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27741-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="27741-132">Чтобы получить дополнительные сведения о поддерживаемом API для конкретной технологии, щелкните ссылку в одной из сводных таблиц, чтобы открыть раздел об этой технологии.</span><span class="sxs-lookup"><span data-stu-id="27741-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="27741-133">В следующей таблице приведены технологии, поддерживаемые для Windows Server 2008 и Windows Server 2003 с обновлением платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="27741-134">Технология</span><span class="sxs-lookup"><span data-stu-id="27741-134">Technology</span></span>                                                                                    | <span data-ttu-id="27741-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27741-135">Windows Server 2008</span></span> | <span data-ttu-id="27741-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27741-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="27741-137">API автоматизации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="27741-138">Да</span><span class="sxs-lookup"><span data-stu-id="27741-138">Yes</span></span>                 | <span data-ttu-id="27741-139">Да</span><span class="sxs-lookup"><span data-stu-id="27741-139">Yes</span></span>                 |
| [<span data-ttu-id="27741-140">Графическая система Windows, работа с образами и библиотека XPS</span><span class="sxs-lookup"><span data-stu-id="27741-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="27741-141">Да</span><span class="sxs-lookup"><span data-stu-id="27741-141">Yes</span></span>                 | <span data-ttu-id="27741-142">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-142">No</span></span>                  |
| [<span data-ttu-id="27741-143">Лента Windows и Библиотека диспетчера анимации</span><span class="sxs-lookup"><span data-stu-id="27741-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="27741-144">Да</span><span class="sxs-lookup"><span data-stu-id="27741-144">Yes</span></span>                 | <span data-ttu-id="27741-145">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-145">No</span></span>                  |
| [<span data-ttu-id="27741-146">Платформа портативных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="27741-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="27741-147">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-147">No</span></span>                  | <span data-ttu-id="27741-148">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="27741-149">Описания поддерживаемых API по технологиям</span><span class="sxs-lookup"><span data-stu-id="27741-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="27741-150">Чтобы получить дополнительные сведения о поддерживаемом API для конкретной технологии, щелкните ссылку в одной из сводных таблиц, чтобы открыть раздел об этой технологии.</span><span class="sxs-lookup"><span data-stu-id="27741-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="27741-151">API автоматизации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="27741-152">Графическая система Windows, работа с образами и библиотека XPS</span><span class="sxs-lookup"><span data-stu-id="27741-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="27741-153">Лента Windows и Библиотека диспетчера анимации</span><span class="sxs-lookup"><span data-stu-id="27741-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="27741-154">Платформа портативных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="27741-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="27741-155">API автоматизации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-155">Windows Automation API</span></span>

<span data-ttu-id="27741-156">API автоматизации Windows 3,0 — это набор библиотек DLL и элементов API, которые позволяют продуктам с поддержкой специальных возможностей (AT) предоставлять лучший доступ к компьютерам для частных лиц, имеющих физические или неограниченные проблемы.</span><span class="sxs-lookup"><span data-stu-id="27741-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="27741-157">Кроме того, поскольку API автоматизации Windows 3,0 позволяет приложениям получать доступ к элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса других приложений и управлять ими, это идеальная технология для реализации автоматизированных средств тестирования.</span><span class="sxs-lookup"><span data-stu-id="27741-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="27741-158">Microsoft Active Accessibility (MSAA) и модель автоматизации пользовательского интерфейса аналогичны тем, что предоставляют средства для предоставления и сбора сведений об элементах пользовательского интерфейса и элементах управления для поддержки специальных возможностей пользовательского интерфейса и автоматизации тестирования программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="27741-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="27741-159">Модель автоматизации пользовательского интерфейса — это реализация спецификации модели автоматизации пользовательского интерфейса Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="27741-160">Это новая технология, которая решает многие из ограничений MSAA.</span><span class="sxs-lookup"><span data-stu-id="27741-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="27741-161">Дополнительные сведения об API-интерфейсе Windows Automation 3,0 см. в разделе [Общие сведения о API автоматизации Windows](/windows/desktop/WinAuto/windows-automation-api-overview).</span><span class="sxs-lookup"><span data-stu-id="27741-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="27741-162">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 поддерживают следующий интерфейс API автоматизации Windows 3,0:</span><span class="sxs-lookup"><span data-stu-id="27741-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="27741-163">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="27741-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="27741-164">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="27741-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="27741-165">Выпуски Windows, подходящие для обновлений</span><span class="sxs-lookup"><span data-stu-id="27741-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="27741-166">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 включают поддержку API-интерфейса автоматизации Windows 3,0 для выпусков Windows, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27741-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27741-167">Версия Windows</span><span class="sxs-lookup"><span data-stu-id="27741-167">Windows Version</span></span></th>
<th><span data-ttu-id="27741-168">Доступные для обновления выпуски</span><span class="sxs-lookup"><span data-stu-id="27741-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27741-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="27741-170">Начальная с пакетом обновления 2 (SP2) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="27741-171">Домашняя базовая с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-172">Домашняя расширенная с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-173">Business с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-174">Enterprise с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-175">Ultimate с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27741-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27741-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="27741-177">Windows XP Home с пакетом обновления 3 (SP2) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="27741-178">Windows XP Professional с пакетом обновления 3 (SP3) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27741-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27741-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="27741-180">Windows Server 2008 с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27741-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27741-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="27741-182">Windows Server 2003 с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="27741-183">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="27741-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="27741-184">Microsoft Active Accessibility (MSAA) — это устаревшая технология, которая впервые появилась в Windows 95.</span><span class="sxs-lookup"><span data-stu-id="27741-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="27741-185">Это набор API-интерфейсов, которые улучшают способ работы продуктов вспомогательных технологий с приложениями, работающими в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="27741-186">API предоставляет программные интерфейсы и методы для предоставления сведений об элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27741-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="27741-187">Дополнительные сведения о Microsoft Active Accessibility см. в [техническом обзоре](/windows/desktop/WinAuto/technical-overview).</span><span class="sxs-lookup"><span data-stu-id="27741-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="27741-188">Поддерживаемые элементы API Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="27741-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="27741-189">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="27741-190">Автоматизация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="27741-190">UI Automation</span></span>

<span data-ttu-id="27741-191">Модель автоматизации пользовательского интерфейса — это новая технология, которая реализует спецификацию модели автоматизации пользовательского интерфейса и устраняет многие из ограничений Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="27741-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="27741-192">Это набор интерфейсов API, обеспечивающих программный доступ к элементам пользовательского интерфейса приложений.</span><span class="sxs-lookup"><span data-stu-id="27741-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="27741-193">Предоставляемые API помогают программным продуктам и автоматизированным средствам тестирования получать доступ, находить стандартные и настраиваемые элементы пользовательского интерфейса приложения, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="27741-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="27741-194">Дополнительные сведения об автоматизации пользовательского интерфейса см. в разделе [API автоматизации Windows: Модель автоматизации пользовательского интерфейса](../winauto/entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="27741-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="27741-195">Поддерживаемые элементы API модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="27741-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="27741-196">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="27741-197">Выполнение автоматизации пользовательского интерфейса в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="27741-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="27741-198">Из-за различий в том, как стандартные элементы управления и стандартные элементы управления Windows реализуются в различных версиях Windows, в информации, которую получают прокси-серверы автоматизации пользовательского интерфейса для этих элементов управления, могут быть незначительные отличия от одной версии к другой.</span><span class="sxs-lookup"><span data-stu-id="27741-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="27741-199">Графическая система Windows, работа с образами и библиотека XPS</span><span class="sxs-lookup"><span data-stu-id="27741-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="27741-200">Обновление платформы для Windows Vista поддерживает следующие API-интерфейсы Windows 7 из библиотеки графики Windows, изображений и XPS:</span><span class="sxs-lookup"><span data-stu-id="27741-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="27741-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="27741-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="27741-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="27741-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="27741-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="27741-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="27741-204">Упаковка</span><span class="sxs-lookup"><span data-stu-id="27741-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="27741-205">Компонент обработки изображений Windows</span><span class="sxs-lookup"><span data-stu-id="27741-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="27741-206">Документ XPS</span><span class="sxs-lookup"><span data-stu-id="27741-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="27741-207">Печать XPS</span><span class="sxs-lookup"><span data-stu-id="27741-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="27741-208">Выпуски Windows, подходящие для обновлений</span><span class="sxs-lookup"><span data-stu-id="27741-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="27741-209">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 включают поддержку графики Windows, работы с образами и библиотекой XPS для выпусков Windows, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27741-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27741-210">Версия Windows</span><span class="sxs-lookup"><span data-stu-id="27741-210">Windows Version</span></span></th>
<th><span data-ttu-id="27741-211">Доступные для обновления выпуски</span><span class="sxs-lookup"><span data-stu-id="27741-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27741-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="27741-213">Начальная с пакетом обновления 2 (SP2) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="27741-214">Домашняя базовая с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-215">Домашняя расширенная с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-216">Business с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-217">Enterprise с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-218">Ultimate с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27741-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27741-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="27741-220">Windows Server 2008 с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="27741-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="27741-221">Direct2D</span></span>

<span data-ttu-id="27741-222">API Direct2D — это новый высокопроизводительный, одноуровневый API-интерфейс с ускорением в режиме быстрого режима, обеспечивающий высокую производительность и высококачественную отрисовку для двухмерной геометрии, точечных рисунков и текста.</span><span class="sxs-lookup"><span data-stu-id="27741-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="27741-223">API Direct2D поддерживает взаимодействие с существующим кодом, использующим GDI, GDI+ или Direct3D.</span><span class="sxs-lookup"><span data-stu-id="27741-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="27741-224">Дополнительные сведения о Direct2D см. в разделе [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span><span class="sxs-lookup"><span data-stu-id="27741-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="27741-225">Поддерживаемые элементы API Direct2D</span><span class="sxs-lookup"><span data-stu-id="27741-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="27741-226">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="27741-227">Запуск Direct2D в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="27741-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="27741-228">Если в Windows Vista отсутствует драйвер WDDM 1,1, производительность взаимодействия Direct2D/GDI будет снижена.</span><span class="sxs-lookup"><span data-stu-id="27741-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="27741-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="27741-229">Direct3D</span></span>

<span data-ttu-id="27741-230">Обновление платформы для Windows Vista обеспечивает поддержку BGRA Surface для Direct3D10 и Direct3D 10.1 Code-paths.</span><span class="sxs-lookup"><span data-stu-id="27741-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="27741-231">Direct3D10Level9 позволяет функции Direct3D10 работать на оборудовании Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="27741-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="27741-232">Direct3D WARP10 — это производительная программа программной прорисовки для Direct3D10 приложений.</span><span class="sxs-lookup"><span data-stu-id="27741-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="27741-233">Direct3D11, последняя версия Direct3D, предоставляет новые возможности, такие как улучшенная поддержка многопоточности, тесселяция, функции DirectCompute и динамическая компоновка шейдера.</span><span class="sxs-lookup"><span data-stu-id="27741-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="27741-234">При создании приложений, использующих Direct3D, [пакет SDK DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) является обязательным.</span><span class="sxs-lookup"><span data-stu-id="27741-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="27741-235">Дополнительные сведения о Direct3D см. в разделе [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27741-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="27741-236">Поддерживаемые элементы API Direct3D</span><span class="sxs-lookup"><span data-stu-id="27741-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="27741-237">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="27741-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="27741-238">DirectWrite</span></span>

<span data-ttu-id="27741-239">API DirectWrite — это новый текстовый API, который предоставляет несколько уровней функциональности, включая макет текста, обработку скриптов, визуализацию глифов и систему шрифтов.</span><span class="sxs-lookup"><span data-stu-id="27741-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="27741-240">DirectWrite использует шрифты OpenType и визуализацию ClearType в виде вспомогательных точек для улучшения текстового интерфейса, предоставляемого приложениями.</span><span class="sxs-lookup"><span data-stu-id="27741-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="27741-241">При использовании с Direct2D для отрисовки текста используется аппаратное ускорение.</span><span class="sxs-lookup"><span data-stu-id="27741-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="27741-242">Дополнительные сведения о DirectWrite см. в разделе [Введение в DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span><span class="sxs-lookup"><span data-stu-id="27741-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="27741-243">Поддерживаемые элементы API DirectWrite</span><span class="sxs-lookup"><span data-stu-id="27741-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="27741-244">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="27741-245">Запуск DirectWrite в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="27741-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="27741-246">Следующие проблемы поведения могут повлиять на использование API DirectWrite в предыдущих версиях Windows:</span><span class="sxs-lookup"><span data-stu-id="27741-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="27741-247">Сценарии, новые для Windows 7, могут неправильно отображаться в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="27741-248">Языковые стандарты, недоступные в предыдущих версиях Windows, переходят к поведению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27741-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="27741-249">Тюнер ClearType недоступен в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="27741-250">Взаимодействие с GDI имеет более высокую стоимость памяти в некоторых сценариях предыдущих версий Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="27741-251">Упаковка</span><span class="sxs-lookup"><span data-stu-id="27741-251">Packaging</span></span>

<span data-ttu-id="27741-252">Обновление платформы для Windows Vista поддерживает ограниченный набор API-интерфейсов упаковки, которые необходимы для выполнения задач с помощью API документов XPS в неуправляемых приложениях.</span><span class="sxs-lookup"><span data-stu-id="27741-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="27741-253">Дополнительные сведения об API упаковки см. в статье [Обзор API упаковки](/previous-versions/windows/desktop/opc/packaging-api-overview).</span><span class="sxs-lookup"><span data-stu-id="27741-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="27741-254">Поддерживаемые элементы API упаковки</span><span class="sxs-lookup"><span data-stu-id="27741-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="27741-255">Поддерживаются только следующие интерфейсы упаковки:</span><span class="sxs-lookup"><span data-stu-id="27741-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="27741-256">иопкури</span><span class="sxs-lookup"><span data-stu-id="27741-256">IOpcUri</span></span>
-   <span data-ttu-id="27741-257">иопкпартури</span><span class="sxs-lookup"><span data-stu-id="27741-257">IOpcPartUri</span></span>
-   <span data-ttu-id="27741-258">Иопкфактори (поддерживаются только следующие методы)</span><span class="sxs-lookup"><span data-stu-id="27741-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="27741-259">креатепаккажерутури</span><span class="sxs-lookup"><span data-stu-id="27741-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="27741-260">креатепартури</span><span class="sxs-lookup"><span data-stu-id="27741-260">CreatePartUri</span></span>
    -   <span data-ttu-id="27741-261">креатестреамонфиле</span><span class="sxs-lookup"><span data-stu-id="27741-261">CreateStreamOnFile</span></span>

<span data-ttu-id="27741-262">Поддерживаемые API упаковки можно использовать для создания потоков по файлам, а также для создания и взаимодействия с универсальным кодом ресурса (URI) на основе пакетов.</span><span class="sxs-lookup"><span data-stu-id="27741-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="27741-263">Запуск API упаковки в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="27741-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="27741-264">Поведение и производительность поддерживаемых интерфейсов упаковки и методов одинаковы на всех поддерживаемых платформах.</span><span class="sxs-lookup"><span data-stu-id="27741-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="27741-265">Если приложение пытается создать экземпляр или вызвать неподдерживаемый интерфейс упаковки или метод, попытка завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="27741-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="27741-266">Если вызов выполняется в неподдерживаемом методе [**иопкфактори**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) , \_ возвращается код ошибки E нотимпл.</span><span class="sxs-lookup"><span data-stu-id="27741-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="27741-267">Компонент обработки изображений Windows</span><span class="sxs-lookup"><span data-stu-id="27741-267">Windows Imaging Component</span></span>

<span data-ttu-id="27741-268">Новые возможности компонента Windows Imaging Component (WIC) включают в себя улучшенную безопасность, поддержку высокого цвета и лучшую совместимость метаданных.</span><span class="sxs-lookup"><span data-stu-id="27741-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="27741-269">Кроме того, компонент создания образов Windows расширяет соответствие стандартам требованиям, предоставляя поддержку для декодирования изображений, расширенных функций PNG, метаданных GIF,, обновлений фотографий HD и метаданных, охватывающих сегменты Аппн.</span><span class="sxs-lookup"><span data-stu-id="27741-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="27741-270">Дополнительные сведения о компоненте создания образов Windows см. в разделе [Общие сведения о компоненте создания образов Windows](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span><span class="sxs-lookup"><span data-stu-id="27741-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="27741-271">Поддерживаемые элементы API WIC</span><span class="sxs-lookup"><span data-stu-id="27741-271">Supported WIC API Elements</span></span>

<span data-ttu-id="27741-272">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="27741-273">Документ XPS</span><span class="sxs-lookup"><span data-stu-id="27741-273">XPS Document</span></span>

<span data-ttu-id="27741-274">API-интерфейсы документов XPS поддерживают создание, изменение и сохранение документов XPS в неуправляемых приложениях.</span><span class="sxs-lookup"><span data-stu-id="27741-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="27741-275">Дополнительные сведения об API документов XPS см. в разделе [руководства по программированию документов XPS.](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27741-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="27741-276">Поддерживаемые элементы API документов XPS</span><span class="sxs-lookup"><span data-stu-id="27741-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="27741-277">Только интерфейсы [цифровых подписей XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) не поддерживаются в версиях ОС нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="27741-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="27741-278">Печать XPS</span><span class="sxs-lookup"><span data-stu-id="27741-278">XPS Print</span></span>

<span data-ttu-id="27741-279">API-интерфейсы печати XPS поддерживают печать документов XPS из приложений на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="27741-280">Дополнительные сведения об API-интерфейсах печати XPS см. в разделе [API кспспринт](/windows/desktop/printdocs/xpsprint-api).</span><span class="sxs-lookup"><span data-stu-id="27741-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="27741-281">Поддерживаемые элементы API печати XPS</span><span class="sxs-lookup"><span data-stu-id="27741-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="27741-282">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="27741-283">Лента Windows и Библиотека диспетчера анимации</span><span class="sxs-lookup"><span data-stu-id="27741-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="27741-284">Обновление платформы для Windows Vista поддерживает следующие API-интерфейсы Windows 7 из ленты Windows и библиотеки анимации.</span><span class="sxs-lookup"><span data-stu-id="27741-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="27741-285">Платформа ленты Windows</span><span class="sxs-lookup"><span data-stu-id="27741-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="27741-286">Диспетчер анимации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="27741-287">Выпуски Windows, подходящие для обновлений</span><span class="sxs-lookup"><span data-stu-id="27741-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="27741-288">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 включают поддержку ленты Windows и библиотеки диспетчера анимации для выпусков Windows, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27741-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27741-289">Версия Windows</span><span class="sxs-lookup"><span data-stu-id="27741-289">Windows Version</span></span></th>
<th><span data-ttu-id="27741-290">Доступные для обновления выпуски</span><span class="sxs-lookup"><span data-stu-id="27741-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27741-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="27741-292">Начальная с пакетом обновления 2 (SP2) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="27741-293">Домашняя базовая с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-294">Домашняя расширенная с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-295">Business с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-296">Enterprise с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-297">Ultimate с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27741-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27741-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="27741-299">Windows Server 2008 с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="27741-300">Платформа ленты Windows</span><span class="sxs-lookup"><span data-stu-id="27741-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="27741-301">Платформа ленты Windows — это обширная система представления команд, которая предоставляет современный вариант для многоуровневых меню, панелей инструментов и панелей задач традиционных приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="27741-302">Платформа — это набор интерфейсов API Microsoft Win32, которые предоставляют возможности создания новых возможностей пользовательского интерфейса для разработчиков Windows и включают в себя как ленту, так и систему контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="27741-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="27741-303">Дополнительные сведения о платформе Ribbon см. в статье [Знакомство с платформой ленты Windows](../windowsribbon/windowsribbon-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="27741-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="27741-304">Поддерживаемые элементы API платформы ленты</span><span class="sxs-lookup"><span data-stu-id="27741-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="27741-305">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="27741-306">Диспетчер анимации Windows</span><span class="sxs-lookup"><span data-stu-id="27741-306">Windows Animation Manager</span></span>

<span data-ttu-id="27741-307">Диспетчер анимации Windows (Windows Animation) — это программный интерфейс, поддерживающий анимацию визуальных элементов приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="27741-308">Анимация Windows призвана упростить разработку и обслуживание последовательностей анимации и позволить разработчикам реализовать единообразные и интуитивно понятные анимации.</span><span class="sxs-lookup"><span data-stu-id="27741-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="27741-309">Анимацию Windows можно использовать с любой графической платформой, включая Direct2D, Direct3D или GDI+.</span><span class="sxs-lookup"><span data-stu-id="27741-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="27741-310">Анимация Windows — это однопотоковый COM-интерфейс API, который предоставляет разработчику все необходимое для создания и управления анимацией пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27741-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="27741-311">Дополнительные сведения о диспетчере анимации Windows см. в разделе [Введение в анимацию Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span><span class="sxs-lookup"><span data-stu-id="27741-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="27741-312">Поддерживаемые элементы API диспетчера анимации</span><span class="sxs-lookup"><span data-stu-id="27741-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="27741-313">Все API-интерфейсы поддерживаются в предыдущих версиях Windows, которые подходят для обновления платформы для Windows Vista или обновления платформы для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="27741-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="27741-314">Платформа портативных устройств Windows</span><span class="sxs-lookup"><span data-stu-id="27741-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="27741-315">Обновление платформы для Windows Vista поддерживает расширения Windows 7 для платформы портативных устройств Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="27741-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="27741-316">Эта функция позволяет компьютерам взаимодействовать с подключенными носителями и устройствами хранения.</span><span class="sxs-lookup"><span data-stu-id="27741-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="27741-317">WPD обеспечивает гибкий и надежный способ обмена данными между компьютерами с цифровыми камерами, музыкальными проигрывателями, мобильными телефонами и многими другими типами подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="27741-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="27741-318">Дополнительные сведения о переносных устройствах Windows см. в разделе [переносные устройства Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .</span><span class="sxs-lookup"><span data-stu-id="27741-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="27741-319">Выпуски Windows, подходящие для обновлений</span><span class="sxs-lookup"><span data-stu-id="27741-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="27741-320">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 включают поддержку портативных устройств Windows (WPD) для выпусков Windows, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="27741-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27741-321">Версия Windows</span><span class="sxs-lookup"><span data-stu-id="27741-321">Windows Version</span></span></th>
<th><span data-ttu-id="27741-322">Доступные для обновления выпуски</span><span class="sxs-lookup"><span data-stu-id="27741-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27741-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="27741-324">Начальная с пакетом обновления 2 (SP2) (x86)</span><span class="sxs-lookup"><span data-stu-id="27741-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="27741-325">Домашняя базовая с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-326">Домашняя расширенная с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-327">Business с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-328">Enterprise с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="27741-329">Ultimate с пакетом обновления 2 (SP2) (x86 и AMD64)</span><span class="sxs-lookup"><span data-stu-id="27741-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="27741-330">Поддерживаемые элементы API WPD</span><span class="sxs-lookup"><span data-stu-id="27741-330">Supported WPD API Elements</span></span>

<span data-ttu-id="27741-331">В следующей таблице перечислены функции, которые поддерживаются в Windows 7, Windows Vista и Windows Vista с обновлением платформы для Windows Vista версий операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="27741-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="27741-332">Компонент WPD</span><span class="sxs-lookup"><span data-stu-id="27741-332">WPD Feature</span></span>                    | <span data-ttu-id="27741-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27741-333">Windows 7</span></span> | <span data-ttu-id="27741-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-334">Windows Vista</span></span> | <span data-ttu-id="27741-335">Windows Vista с обновлением платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="27741-336">MTP по USB</span><span class="sxs-lookup"><span data-stu-id="27741-336">MTP over USB</span></span>                   | <span data-ttu-id="27741-337">Да</span><span class="sxs-lookup"><span data-stu-id="27741-337">Yes</span></span>       | <span data-ttu-id="27741-338">Да</span><span class="sxs-lookup"><span data-stu-id="27741-338">Yes</span></span>           | <span data-ttu-id="27741-339">Да</span><span class="sxs-lookup"><span data-stu-id="27741-339">Yes</span></span>                                                  |
| <span data-ttu-id="27741-340">MTP по IP</span><span class="sxs-lookup"><span data-stu-id="27741-340">MTP over IP</span></span>                    | <span data-ttu-id="27741-341">Да</span><span class="sxs-lookup"><span data-stu-id="27741-341">Yes</span></span>       | <span data-ttu-id="27741-342">Да</span><span class="sxs-lookup"><span data-stu-id="27741-342">Yes</span></span>           | <span data-ttu-id="27741-343">Да</span><span class="sxs-lookup"><span data-stu-id="27741-343">Yes</span></span>                                                  |
| <span data-ttu-id="27741-344">MTP по Bluetooth</span><span class="sxs-lookup"><span data-stu-id="27741-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="27741-345">Да</span><span class="sxs-lookup"><span data-stu-id="27741-345">Yes</span></span>       | <span data-ttu-id="27741-346">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-346">No</span></span>            | <span data-ttu-id="27741-347">Да</span><span class="sxs-lookup"><span data-stu-id="27741-347">Yes</span></span>                                                  |
| <span data-ttu-id="27741-348">Службы устройств WPD и MTP</span><span class="sxs-lookup"><span data-stu-id="27741-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="27741-349">Да</span><span class="sxs-lookup"><span data-stu-id="27741-349">Yes</span></span>       | <span data-ttu-id="27741-350">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-350">No</span></span>            | <span data-ttu-id="27741-351">Да</span><span class="sxs-lookup"><span data-stu-id="27741-351">Yes</span></span>                                                  |
| <span data-ttu-id="27741-352">Автоматизация WPD</span><span class="sxs-lookup"><span data-stu-id="27741-352">WPD Automation</span></span>                 | <span data-ttu-id="27741-353">Да</span><span class="sxs-lookup"><span data-stu-id="27741-353">Yes</span></span>       | <span data-ttu-id="27741-354">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-354">No</span></span>            | <span data-ttu-id="27741-355">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-355">No</span></span>                                                   |
| <span data-ttu-id="27741-356">Множественная функция/множественное транспортировка</span><span class="sxs-lookup"><span data-stu-id="27741-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="27741-357">Да</span><span class="sxs-lookup"><span data-stu-id="27741-357">Yes</span></span>       | <span data-ttu-id="27741-358">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-358">No</span></span>            | <span data-ttu-id="27741-359">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-359">No</span></span>                                                   |
| <span data-ttu-id="27741-360">Этап устройства</span><span class="sxs-lookup"><span data-stu-id="27741-360">Device Stage</span></span>                   | <span data-ttu-id="27741-361">Да</span><span class="sxs-lookup"><span data-stu-id="27741-361">Yes</span></span>       | <span data-ttu-id="27741-362">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-362">No</span></span>            | <span data-ttu-id="27741-363">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-363">No</span></span>                                                   |
| <span data-ttu-id="27741-364">Платформа синхронизации устройств</span><span class="sxs-lookup"><span data-stu-id="27741-364">Device Sync Platform</span></span>           | <span data-ttu-id="27741-365">Да</span><span class="sxs-lookup"><span data-stu-id="27741-365">Yes</span></span>       | <span data-ttu-id="27741-366">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-366">No</span></span>            | <span data-ttu-id="27741-367">Нет</span><span class="sxs-lookup"><span data-stu-id="27741-367">No</span></span>                                                   |



 

<span data-ttu-id="27741-368">Для выпусков Windows 7 и Windows Vista, на которых не установлен проигрыватель Microsoft Windows Media по умолчанию (выпуски N и KN), необходимо установить [пакет SDK для формата Windows Media 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) для включения функции WPD.</span><span class="sxs-lookup"><span data-stu-id="27741-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="27741-369">Дополнительные сведения см. в [статье базы знаний](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) которая была изначально опубликована как решение для Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="27741-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27741-370">См. также</span><span class="sxs-lookup"><span data-stu-id="27741-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27741-371">Обновление платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="27741-372">**Разделы общих сведений**</span><span class="sxs-lookup"><span data-stu-id="27741-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="27741-373">Сведения об обновлении платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27741-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="27741-374">Статья базы знаний об обновлении платформы для Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="27741-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
---
title: Устранение проблем с упаковкой и развертыванием приложений для Windows, а также с обращением к ним
description: Используйте эти рекомендации для устранения неполадок, возникающих при упаковке, развертывании или выполнении запросов к пакету приложения.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "105708632"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="0646b-103">Устранение проблем с упаковкой и развертыванием приложений для Windows, а также с обращением к ним</span><span class="sxs-lookup"><span data-stu-id="0646b-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="0646b-104">Используйте эти рекомендации для устранения неполадок, возникающих при упаковке, развертывании или запросе пакета приложения Windows (. msix/. appx) в качестве разработчика.</span><span class="sxs-lookup"><span data-stu-id="0646b-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="0646b-105">Эта статья предназначена для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="0646b-105">This article is intended for developers.</span></span> <span data-ttu-id="0646b-106">Если вы не являетесь разработчиком и ищете справку по ошибке установки приложения Windows, см. раздел [Поддержка Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="0646b-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="0646b-107">Получение диагностических сведений</span><span class="sxs-lookup"><span data-stu-id="0646b-107">Get diagnostic information</span></span>

<span data-ttu-id="0646b-108">При сбое API возвращается код ошибки, описывающий проблему.</span><span class="sxs-lookup"><span data-stu-id="0646b-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="0646b-109">Если код ошибки не содержит достаточно сведений, вы найдете дополнительные диагностические сведения в подробных журналах событий.</span><span class="sxs-lookup"><span data-stu-id="0646b-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="0646b-110">Чтобы получить доступ к журналам событий упаковки и развертывания с помощью **Просмотр событий**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0646b-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="0646b-111">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="0646b-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="0646b-112">Нажмите кнопку **Пуск** в меню Windows, введите **Просмотр событий** и **нажмите клавишу ВВОД**.</span><span class="sxs-lookup"><span data-stu-id="0646b-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="0646b-113">Запустите **eventvwr. msc**.</span><span class="sxs-lookup"><span data-stu-id="0646b-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="0646b-114">На левой странице разверните узел **Просмотр событий (локальные)**  >  **приложения и службы журналы**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="0646b-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="0646b-115">Проверьте наличие доступных журналов в следующих категориях:</span><span class="sxs-lookup"><span data-stu-id="0646b-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="0646b-116">**AppxPackagingOM**  >  **Microsoft-Windows-аппкспаккагинг/эксплуатация**</span><span class="sxs-lookup"><span data-stu-id="0646b-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="0646b-117">**AppXDeployment — сервер**  >  **Microsoft-Windows-AppXDeploymentServer/эксплуатация**</span><span class="sxs-lookup"><span data-stu-id="0646b-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="0646b-118">Начните с просмотра журналов в разделе **AppXDeployment-Server**.</span><span class="sxs-lookup"><span data-stu-id="0646b-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="0646b-119">Если ошибка вызвана **0x80073CF0** или **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, в журналах **AppxpackagingOM** могут присутствовать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0646b-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="0646b-120">Вы также можете использовать команду [Get-аппкслог](/powershell/module/appx/get-appxlog) в PowerShell, чтобы получить первые несколько зарегистрированных событий.</span><span class="sxs-lookup"><span data-stu-id="0646b-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="0646b-121">В следующем примере отображаются журналы, связанные с последней операцией развертывания.</span><span class="sxs-lookup"><span data-stu-id="0646b-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="0646b-122">В следующем примере отображаются журналы, связанные с последней операцией развертывания в интерактивной таблице в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="0646b-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="0646b-123">Коды распространенных ошибок</span><span class="sxs-lookup"><span data-stu-id="0646b-123">Common error codes</span></span>

<span data-ttu-id="0646b-124">В этой таблице перечислены некоторые из наиболее распространенных кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="0646b-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="0646b-125">Если вам нужна дополнительная помощь по одной из этих ошибок или если вы столкнулись с кодом ошибки, отсутствующим в этом списке, см. раздел [Дополнительные параметры справки](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="0646b-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0646b-126">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="0646b-126">Error code</span></span></th>
<th><span data-ttu-id="0646b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0646b-127">Value</span></span></th>
<th><span data-ttu-id="0646b-128">Описание и возможные причины</span><span class="sxs-lookup"><span data-stu-id="0646b-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="0646b-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="0646b-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="0646b-130">0x80070002</span></span></td>
<td><span data-ttu-id="0646b-131">Файл или путь не найден.</span><span class="sxs-lookup"><span data-stu-id="0646b-131">File or path is not found.</span></span> <span data-ttu-id="0646b-132">Это может произойти во время проверки библиотеки типов COM, так как в рамках пакета MSIX путь к каталогу действительно существует.</span><span class="sxs-lookup"><span data-stu-id="0646b-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="0646b-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="0646b-134">0x8007000B</span></span></td>
<td><span data-ttu-id="0646b-135">Пакет имеет неправильный формат и нуждается в повторной сборке или повторной подписи.</span><span class="sxs-lookup"><span data-stu-id="0646b-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="0646b-136">Эта ошибка может возникнуть в случае несоответствия между именем субъекта сертификата подписи и именем издателя AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="0646b-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="0646b-137">См. раздел <a href="how-to-sign-a-package-using-signtool.md">как подписать пакет приложения с помощью средства SignTool</a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="0646b-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="0646b-139">0x80070057</span></span></td>
<td><span data-ttu-id="0646b-140">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="0646b-140">One or more arguments are not valid.</span></span> <span data-ttu-id="0646b-141">Если проверить журнал событий AppXDeployment-Server и просмотреть следующее событие: "при установке пакета система не смогла зарегистрировать расширение Windows. Репоситорекстенсион из-за следующей ошибки: неправильный параметр".</span><span class="sxs-lookup"><span data-stu-id="0646b-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="0646b-142">Эта ошибка может возникать, если элементы манифеста DisplayName или Description содержат символы, запрещенные брандмауэром Windows. а именно |  и все, из-за того, что Windows не удалось создать профиль AppContainer для пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="0646b-143">Удалите эти символы из манифеста и попробуйте установить пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="0646b-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="0646b-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="0646b-147">Не удалось открыть пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="0646b-148">Возможные причины.</span><span class="sxs-lookup"><span data-stu-id="0646b-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="0646b-149">Пакет не подписан.</span><span class="sxs-lookup"><span data-stu-id="0646b-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="0646b-150">Имя издателя не соответствует субъекту сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="0646b-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="0646b-151">Отсутствует префикс file://, или не удалось найти пакет в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="0646b-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="0646b-152">Дополнительные сведения см. в журнале событий <strong>AppxPackagingOM</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="0646b-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="0646b-156">Не удалось найти пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="0646b-157">Эта ошибка может возникнуть при удалении пакета, который не установлен для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="0646b-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-159"><strong>ПАКЕТЫ</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="0646b-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="0646b-161">Данные пакета недопустимы.</span><span class="sxs-lookup"><span data-stu-id="0646b-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="0646b-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="0646b-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="0646b-165">Пакет не прошел проверку обновлений, зависимостей или конфликтов.</span><span class="sxs-lookup"><span data-stu-id="0646b-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="0646b-166">Возможные причины.</span><span class="sxs-lookup"><span data-stu-id="0646b-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="0646b-167">Входящий пакет конфликтует с установленным пакетом.</span><span class="sxs-lookup"><span data-stu-id="0646b-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="0646b-168">Не удается найти указанную зависимость пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="0646b-169">Пакет не поддерживает правильную архитектуру процессора.</span><span class="sxs-lookup"><span data-stu-id="0646b-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="0646b-170">Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="0646b-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="0646b-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="0646b-174">На компьютере недостаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="0646b-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="0646b-175">Освободите место и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="0646b-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="0646b-177"><strong>СОСТОЯНИЕ</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="0646b-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="0646b-179">Не удается скачать пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="0646b-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="0646b-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="0646b-183">Не удается зарегистрировать пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-183">The package can't be registered.</span></span><br/> <span data-ttu-id="0646b-184">Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="0646b-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="0646b-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="0646b-188">Не удается отменить регистрацию пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="0646b-189">Эта ошибка может возникнуть при удалении пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="0646b-190">Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="0646b-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="0646b-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="0646b-193">Пользователь отменил запрос на установку.</span><span class="sxs-lookup"><span data-stu-id="0646b-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="0646b-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="0646b-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="0646b-196">Не удалось установить пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-196">Package install failed.</span></span> <span data-ttu-id="0646b-197">Обратитесь к поставщику программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0646b-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="0646b-198">Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="0646b-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="0646b-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="0646b-201">Не удалось удалить пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-201">Package removal failed.</span></span><br/> <span data-ttu-id="0646b-202">Эта ошибка может возникнуть при сбоях при удалении пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="0646b-203">Дополнительные сведения см. в разделе <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>ремовепаккажеасинк</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="0646b-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="0646b-207">Предоставленный пакет уже установлен, и переустановка пакета заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0646b-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="0646b-208">Эта ошибка может возникать при установке пакета, который не является побитовым, идентичным пакету, который уже установлен.</span><span class="sxs-lookup"><span data-stu-id="0646b-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="0646b-209">Обратите внимание, что цифровая подпись также является частью пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="0646b-210">Следовательно, если пакет перестраивается или повторно подписан, он больше не будет побитовым, идентичным ранее установленному пакету.</span><span class="sxs-lookup"><span data-stu-id="0646b-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="0646b-211">Существует два возможных варианта исправления этой ошибки: (1) увеличение номера версии приложения, затем повторное создание и повторная подпись пакета (2) удаление старого пакета для каждого пользователя в системе перед установкой нового пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="0646b-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="0646b-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="0646b-214">Не удается запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="0646b-214">The app can't be started.</span></span> <span data-ttu-id="0646b-215">Попробуйте переустановить приложение.</span><span class="sxs-lookup"><span data-stu-id="0646b-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="0646b-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="0646b-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="0646b-219">Не удалось удовлетворить указанную предварительную проверку.</span><span class="sxs-lookup"><span data-stu-id="0646b-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="0646b-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="0646b-223">Репозиторий пакетов поврежден.</span><span class="sxs-lookup"><span data-stu-id="0646b-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="0646b-224">Эта ошибка может возникать, если папка, на которую ссылается этот раздел реестра, не существует или повреждена:</span><span class="sxs-lookup"><span data-stu-id="0646b-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="0646b-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="0646b-226"><strong>куррентверсион\аппкс\паккажерепоситорирут</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="0646b-227">Для восстановления после этого состояния обновите компьютер.</span><span class="sxs-lookup"><span data-stu-id="0646b-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="0646b-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="0646b-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="0646b-231">Для установки этого приложения требуется лицензия разработчика или система, поддерживающая загрузку неопубликованных приложений.</span><span class="sxs-lookup"><span data-stu-id="0646b-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="0646b-232">Эта ошибка может возникнуть, если пакет не соответствует одному из следующих требований:</span><span class="sxs-lookup"><span data-stu-id="0646b-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="0646b-233">Приложение развертывается с помощью F5 в Visual Studio на компьютере с лицензией разработчика Windows.</span><span class="sxs-lookup"><span data-stu-id="0646b-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="0646b-234">Пакет подписывается подписью Майкрософт и развертывается как часть Windows или из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0646b-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="0646b-235">Пакет подписывается доверенной подписью и устанавливается на компьютере с лицензией разработчика, присоединенным к домену компьютеру с включенной политикой AllowAllTrustedApps или на компьютере с лицензией на загрузку неопубликованных приложений Windows с включенной политикой AllowAllTrustedApps.</span><span class="sxs-lookup"><span data-stu-id="0646b-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="0646b-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="0646b-237">0x80073D00</span></span></td>
<td><span data-ttu-id="0646b-238">Не удается запустить приложение, так как оно сейчас обновляется.</span><span class="sxs-lookup"><span data-stu-id="0646b-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="0646b-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="0646b-241">0x80073D01</span></span></td>
<td><span data-ttu-id="0646b-242">Операция развертывания пакета заблокирована политикой.</span><span class="sxs-lookup"><span data-stu-id="0646b-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="0646b-243">Обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="0646b-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="0646b-244">Возможные причины.</span><span class="sxs-lookup"><span data-stu-id="0646b-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="0646b-245">Развертывание пакетов блокируется политиками управления приложениями.</span><span class="sxs-lookup"><span data-stu-id="0646b-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="0646b-246">Развертывание пакета блокируется с помощью &quot; политики разрешить операции развертывания в особых профилях &quot; .</span><span class="sxs-lookup"><span data-stu-id="0646b-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="0646b-247">Одна из возможных причин — потребность в перемещаемом профиле.</span><span class="sxs-lookup"><span data-stu-id="0646b-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="0646b-248">Сведения о настройке перемещаемых профилей пользователей в учетных записях пользователей см. в статье <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">развертывание перемещаемых профилей пользователей</a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="0646b-249">Если в системе нет настроенных политик и вы по-прежнему видите эту ошибку, возможно, вы выполнили вход с временным профилем.</span><span class="sxs-lookup"><span data-stu-id="0646b-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="0646b-250">Выйдите из журнала и снова войдите в систему, а затем повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="0646b-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="0646b-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="0646b-252">0x80073D02</span></span></td>
<td><span data-ttu-id="0646b-253">Не удалось установить пакет, так как ресурсы, которые он изменяет, сейчас используются.</span><span class="sxs-lookup"><span data-stu-id="0646b-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="0646b-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="0646b-256">0x80073D03</span></span></td>
<td><span data-ttu-id="0646b-257">Не удалось восстановить пакет, так как данные, необходимые для восстановления, повреждены.</span><span class="sxs-lookup"><span data-stu-id="0646b-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="0646b-260">0x80073D04</span></span></td>
<td><span data-ttu-id="0646b-261">Недопустимая подпись.</span><span class="sxs-lookup"><span data-stu-id="0646b-261">The signature isn't valid.</span></span> <span data-ttu-id="0646b-262">Для регистрации в режиме разработчика необходимо, чтобы AppxSignature. p7x и AppxBlockMap.xml были допустимыми или не должны присутствовать.</span><span class="sxs-lookup"><span data-stu-id="0646b-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="0646b-263">Если вы разработчик, использующий клавишу F5 в Visual Studio, убедитесь, что каталог проекта не содержит сигнатуры или файлы схемы блокировки из предыдущих версий пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="0646b-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="0646b-266">0x80073D05</span></span></td>
<td><span data-ttu-id="0646b-267">Произошла ошибка при удалении ранее существующих данных приложения пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="0646b-268">Эта ошибка может возникнет, если <a href="/previous-versions/hh441475(v=vs.110)">симулятор</a> работает.</span><span class="sxs-lookup"><span data-stu-id="0646b-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="0646b-269">Закройте симулятор.</span><span class="sxs-lookup"><span data-stu-id="0646b-269">Close the simulator.</span></span> <span data-ttu-id="0646b-270">Эту ошибку также можно получить, если в данных приложения открыты файлы (например, если в текстовом редакторе открыт файл журнала).</span><span class="sxs-lookup"><span data-stu-id="0646b-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="0646b-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="0646b-273">0x80073D06</span></span></td>
<td><span data-ttu-id="0646b-274">Не удалось установить пакет, так как уже установлена более поздняя версия этого пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="0646b-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="0646b-277">0x80073D07</span></span></td>
<td><span data-ttu-id="0646b-278">Обнаружена ошибка в системном двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="0646b-278">An error in a system binary was detected.</span></span> <span data-ttu-id="0646b-279">Чтобы устранить эту проблему, попробуйте обновить компьютер.</span><span class="sxs-lookup"><span data-stu-id="0646b-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="0646b-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="0646b-282">0x80073D08</span></span></td>
<td><span data-ttu-id="0646b-283">В системе обнаружен поврежденный двоичный файл, отличный от Windows.</span><span class="sxs-lookup"><span data-stu-id="0646b-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="0646b-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="0646b-286">0x80073D09</span></span></td>
<td><span data-ttu-id="0646b-287">Не удалось возобновить операцию, так как данные, необходимые для восстановления, повреждены.</span><span class="sxs-lookup"><span data-stu-id="0646b-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="0646b-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="0646b-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="0646b-291">Не удалось установить пакет, так как служба брандмауэра Windows не запущена.</span><span class="sxs-lookup"><span data-stu-id="0646b-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="0646b-292">Включите службу брандмауэра Windows и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="0646b-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="0646b-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="0646b-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="0646b-295">Сбой операции перемещения пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="0646b-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="0646b-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="0646b-299">Не удалось выполнить операцию развертывания, так как том не пуст.</span><span class="sxs-lookup"><span data-stu-id="0646b-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="0646b-301"><strong>РАБОТА</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="0646b-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="0646b-303">Не удалось выполнить операцию развертывания, так как том находится вне сети.</span><span class="sxs-lookup"><span data-stu-id="0646b-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="0646b-304">Для обновления пакета том ссылается на установленный том всех версий пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="0646b-306"><strong>ПОВРЕЖДЕН</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="0646b-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="0646b-308">Не удалось выполнить операцию развертывания, так как указанный том поврежден.</span><span class="sxs-lookup"><span data-stu-id="0646b-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="0646b-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="0646b-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="0646b-311">Не удалось выполнить операцию развертывания, так как указанное приложение должно быть зарегистрировано в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="0646b-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="0646b-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="0646b-314">0x80073D10</span></span></td>
<td><span data-ttu-id="0646b-315">Не удалось выполнить операцию развертывания, так как пакет предназначен для неверной архитектуры процессора.</span><span class="sxs-lookup"><span data-stu-id="0646b-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="0646b-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="0646b-318">0x80073D11</span></span></td>
<td><span data-ttu-id="0646b-319">Достигнуто максимальное число пакетов загруженные неопубликованные для разработчиков, разрешенных на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="0646b-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="0646b-320">Удалите пакет загруженные неопубликованные и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="0646b-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="0646b-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="0646b-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="0646b-324">0x80073D12</span></span></td>
<td><span data-ttu-id="0646b-325">Для установки этого дополнительного пакета требуется основной пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="0646b-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="0646b-326">Сначала установите основной пакет и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="0646b-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="0646b-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="0646b-329">0x80073D13</span></span></td>
<td><span data-ttu-id="0646b-330">Этот тип пакета приложения не поддерживается в этой файловой системе.</span><span class="sxs-lookup"><span data-stu-id="0646b-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="0646b-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="0646b-333">0x80073D14</span></span></td>
<td><span data-ttu-id="0646b-334">Операция перемещения пакета блокируется до завершения потоковой передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="0646b-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="0646b-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="0646b-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="0646b-338">0x80073D15</span></span></td>
<td><span data-ttu-id="0646b-339">Основной или другой необязательный пакет приложения имеет тот же идентификатор приложения, что и этот дополнительный пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="0646b-340">Измените идентификатор приложения для дополнительного пакета, чтобы избежать конфликтов.</span><span class="sxs-lookup"><span data-stu-id="0646b-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="0646b-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="0646b-343">0x80073D16</span></span></td>
<td><span data-ttu-id="0646b-344">Этот промежуточный сеанс удерживается, чтобы можно было задать приоритет для другой промежуточной операции.</span><span class="sxs-lookup"><span data-stu-id="0646b-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="0646b-347">0x80073D17</span></span></td>
<td><span data-ttu-id="0646b-348">Связанный набор не может быть обновлен, так как обновленный набор является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="0646b-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="0646b-349">Все пакеты в связанном наборе должны быть обновлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="0646b-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="0646b-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="0646b-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="0646b-353">0x80073D18</span></span></td>
<td><span data-ttu-id="0646b-354">Необязательный пакет с точкой входа FullTrust требует, чтобы основной пакет имел возможность <strong>рунфуллтруст</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="0646b-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="0646b-357">0x80073D19</span></span></td>
<td><span data-ttu-id="0646b-358">Произошла ошибка, так как пользователь вышел из системы.</span><span class="sxs-lookup"><span data-stu-id="0646b-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="0646b-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="0646b-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="0646b-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="0646b-363">Для необязательной подготовки пакета требуется также подготовка основного пакета зависимостей.</span><span class="sxs-lookup"><span data-stu-id="0646b-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="0646b-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="0646b-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="0646b-367">Пакеты не прошли <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">проверку репутации SmartScreen</a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="0646b-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="0646b-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="0646b-371">Истекло время ожидания операции <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">проверки репутации SmartScreen</a> .</span><span class="sxs-lookup"><span data-stu-id="0646b-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="0646b-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="0646b-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="0646b-375">Текущий вариант развертывания не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0646b-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="0646b-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="0646b-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="0646b-379">Активация заблокирована из-за параметров обновления. appinstaller для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="0646b-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="0646b-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="0646b-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="0646b-383">Удаленные диски не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0646b-383">Remote drives are not supported.</span></span> <span data-ttu-id="0646b-384">Используйте <strong> \\ server\share</strong> для регистрации удаленного пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="0646b-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="0646b-387">0x80073D20</span></span></td>
<td><span data-ttu-id="0646b-388">Не удалось обработать и записать Скачанные данные пакета на диск.</span><span class="sxs-lookup"><span data-stu-id="0646b-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="0646b-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="0646b-391">0x80073D21</span></span></td>
<td><span data-ttu-id="0646b-392">Операция развертывания была заблокирована из-за политики семейства пакетов, запрещающей развертывания на несистемном томе.</span><span class="sxs-lookup"><span data-stu-id="0646b-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="0646b-393">Для каждой политики это приложение должно быть установлено на системный диск, но не задано по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0646b-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="0646b-394">В области Параметры хранилища сделайте системный диск используемым по умолчанию, чтобы сохранить новое содержимое, а затем повторите попытку установки.</span><span class="sxs-lookup"><span data-stu-id="0646b-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="0646b-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="0646b-397">0x80073D22</span></span></td>
<td><span data-ttu-id="0646b-398">Операция развертывания была заблокирована из-за того, что политики на уровне компьютера ограничивают развертывания на несистемном томе.</span><span class="sxs-lookup"><span data-stu-id="0646b-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="0646b-399">Для каждой политики это приложение должно быть установлено на системный диск, но не задано по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0646b-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="0646b-400">В области Параметры хранилища сделайте системный диск используемым по умолчанию, чтобы сохранить новое содержимое, а затем повторите попытку установки.</span><span class="sxs-lookup"><span data-stu-id="0646b-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="0646b-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="0646b-403">0x80073D23</span></span></td>
<td><span data-ttu-id="0646b-404">Операция развертывания была заблокирована, так как не разрешается использовать специальное развертывание профиля (специальные профили — это профили пользователей, в которых изменения удаляются после выхода пользователя из программы).</span><span class="sxs-lookup"><span data-stu-id="0646b-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="0646b-405">Попробуйте войти в учетную запись, которая не является специальным профилем.</span><span class="sxs-lookup"><span data-stu-id="0646b-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="0646b-406">Вы можете попробовать выйти из учетной записи и войти в нее снова или войти в другую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0646b-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="0646b-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-409"><strong>КАТАЛОГИ</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="0646b-410">0x80073D24</span></span></td>
<td><span data-ttu-id="0646b-411">Не удалось выполнить операцию развертывания из-за конфликта <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">изменяемого каталога пакета</a>пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="0646b-412">Чтобы установить этот пакет, удалите существующий пакет с конфликтующим изменяемым каталогом пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="0646b-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="0646b-415">0x80073D25</span></span></td>
<td><span data-ttu-id="0646b-416">Не удалось установить пакет, так как был указан одноэлементный ресурс, а другой пользователь с установленным пакетом вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="0646b-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="0646b-417">Убедитесь, что все активные пользователи с установленным пакетом, вышли из системы, и повторите попытку установки.</span><span class="sxs-lookup"><span data-stu-id="0646b-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="0646b-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="0646b-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="0646b-420">0x80073D26</span></span></td>
<td><span data-ttu-id="0646b-421">Произошел сбой установки пакета, так как установлена другая версия службы.</span><span class="sxs-lookup"><span data-stu-id="0646b-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="0646b-422">Попробуйте установить более новую версию пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="0646b-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="0646b-425">0x80073D27</span></span></td>
<td><span data-ttu-id="0646b-426">Произошел сбой установки пакета, так как версия службы существует за пределами пакета. msix/. appx.</span><span class="sxs-lookup"><span data-stu-id="0646b-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="0646b-427">Обратитесь к поставщику программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0646b-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="0646b-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="0646b-430">0x80073D28</span></span></td>
<td><span data-ttu-id="0646b-431">Не удалось установить пакет, так как требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="0646b-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="0646b-432">Обратитесь к администратору, чтобы установить этот пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="0646b-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="0646b-435">0x80073D29</span></span></td>
<td><span data-ttu-id="0646b-436">Не удалось выполнить развертывание пакета, так как операция была перенаправлена на учетную запись по умолчанию, когда вызывающий объект не сделает этого.</span><span class="sxs-lookup"><span data-stu-id="0646b-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="0646b-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="0646b-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="0646b-440">Не удалось выполнить развертывание пакета, так как для пакета требуется возможность, предназначенная для этого узла изначально.</span><span class="sxs-lookup"><span data-stu-id="0646b-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="0646b-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="0646b-444">Не удалось выполнить развертывание пакета, так как его содержимое недопустимо для неподписанного пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="0646b-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="0646b-448">Не удалось выполнить развертывание пакета, так как его издатель отсутствует в неподписанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0646b-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="0646b-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="0646b-452">Не удалось выполнить развертывание пакета, так как его издатель отсутствует в подписанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0646b-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="0646b-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="0646b-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="0646b-456">Не удалось выполнить развертывание пакета, так как его издатель отсутствует в подписанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="0646b-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="0646b-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="0646b-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="0646b-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="0646b-461">Зависимость среды выполнения узла, разрешающая пакет с содержимым с полным доверием, требует, чтобы основной пакет имел возможность <strong>рунфуллтруст</strong> .</span><span class="sxs-lookup"><span data-stu-id="0646b-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="0646b-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="0646b-463">0x80080200</span></span></td>
<td><span data-ttu-id="0646b-464">В API упаковки произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="0646b-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="0646b-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="0646b-467">0x80080201</span></span></td>
<td><span data-ttu-id="0646b-468">Пакет является недопустимым, так как его содержимое чередование.</span><span class="sxs-lookup"><span data-stu-id="0646b-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="0646b-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="0646b-471">0x80080202</span></span></td>
<td><span data-ttu-id="0646b-472">Пакет является недопустимым, так как он содержит связи OPC.</span><span class="sxs-lookup"><span data-stu-id="0646b-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="0646b-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="0646b-475">0x80080203</span></span></td>
<td><span data-ttu-id="0646b-476">Пакет является недопустимым, так как в нем отсутствует манифест или сопоставлена блокировка, или имеется файл с целостностью кода, но отсутствует файл сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="0646b-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="0646b-477">Убедитесь, что в пакете отсутствует один или несколько необходимых файлов:</span><span class="sxs-lookup"><span data-stu-id="0646b-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="0646b-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="0646b-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="0646b-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="0646b-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="0646b-480">Если пакет содержит \Аппксметадата\кодеинтегрити.Кат, он также должен содержать \AppxSignature.p7x.</span><span class="sxs-lookup"><span data-stu-id="0646b-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="0646b-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="0646b-482">0x80080204</span></span></td>
<td><span data-ttu-id="0646b-483">Недопустимый файл AppxManifest.xml пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="0646b-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="0646b-485">0x80080205</span></span></td>
<td><span data-ttu-id="0646b-486">Недопустимый файл AppxBlockMap.xml пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="0646b-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="0646b-488">0x80080206</span></span></td>
<td><span data-ttu-id="0646b-489">Не удается прочитать содержимое пакета, так как оно повреждено.</span><span class="sxs-lookup"><span data-stu-id="0646b-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="0646b-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="0646b-492">0x80080207</span></span></td>
<td><span data-ttu-id="0646b-493">Вычисленное хэш-значение блока не соответствует значению, хранящемуся в карте блоков.</span><span class="sxs-lookup"><span data-stu-id="0646b-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="0646b-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="0646b-496">0x80080208</span></span></td>
<td><span data-ttu-id="0646b-497">Запрошенный диапазон байтов превышает 4 ГБ при преобразовании в диапазон байтов блоков.</span><span class="sxs-lookup"><span data-stu-id="0646b-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="0646b-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="0646b-499">0x800B0100</span></span></td>
<td><span data-ttu-id="0646b-500">В теме отсутствует подпись.</span><span class="sxs-lookup"><span data-stu-id="0646b-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="0646b-501">Эта ошибка может возникать, если пакет не подписан или подпись недействительна.</span><span class="sxs-lookup"><span data-stu-id="0646b-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="0646b-502">Пакет должен быть подписан для развертывания.</span><span class="sxs-lookup"><span data-stu-id="0646b-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="0646b-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="0646b-504">0x800B0109</span></span></td>
<td><span data-ttu-id="0646b-505">Цепочка сертификатов обработана, но была прервана в корневом сертификате, который не является доверенным для поставщика доверия.</span><span class="sxs-lookup"><span data-stu-id="0646b-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="0646b-506">См. раздел <a href="/previous-versions/br230260(v=vs.110)">Подписывание пакета</a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="0646b-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="0646b-508">0x800B010A</span></span></td>
<td><span data-ttu-id="0646b-509">Не удалось построить цепочку сертификатов для доверенного корневого центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="0646b-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="0646b-510">См. раздел <a href="/previous-versions/br230260(v=vs.110)">Подписывание пакета</a>.</span><span class="sxs-lookup"><span data-stu-id="0646b-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="0646b-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="0646b-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="0646b-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="0646b-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="0646b-513">0x80080209</span></span></td>
<td><span data-ttu-id="0646b-514">Структура <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>, используемая для подписи пакета, не содержит необходимых данных</span><span class="sxs-lookup"><span data-stu-id="0646b-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="0646b-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="0646b-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="0646b-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="0646b-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="0646b-517">0x8008020A</span></span></td>
<td><span data-ttu-id="0646b-518">Структура <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> , используемая для шифрования или расшифровки пакета, содержит недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="0646b-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-520"><strong>контентграупмап</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="0646b-521">0x8008020B</span></span></td>
<td><span data-ttu-id="0646b-522">Сопоставленная группа содержимого пакета. msix/. appx недопустима.</span><span class="sxs-lookup"><span data-stu-id="0646b-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="0646b-525">0x8008020C</span></span></td>
<td><span data-ttu-id="0646b-526">Недопустимый <a href="/windows/msix/app-installer/app-installer-root">файл appinstaller</a> для пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="0646b-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="0646b-529">0x8008020D</span></span></td>
<td><span data-ttu-id="0646b-530">Базовая версия пакета в разностном пакете не соответствует версии базового пакета для обновления.</span><span class="sxs-lookup"><span data-stu-id="0646b-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="0646b-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="0646b-533">0x8008020E</span></span></td>
<td><span data-ttu-id="0646b-534">В разностном пакете отсутствует файл из обновленного пакета.</span><span class="sxs-lookup"><span data-stu-id="0646b-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="0646b-537">0x8008020F</span></span></td>
<td><span data-ttu-id="0646b-538">Недопустимый разностный пакет.</span><span class="sxs-lookup"><span data-stu-id="0646b-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="0646b-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="0646b-541">0x80080210</span></span></td>
<td><span data-ttu-id="0646b-542">Добавленный Дельта-пакет не разрешен для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="0646b-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="0646b-545">0x80080211</span></span></td>
<td><span data-ttu-id="0646b-546">Недопустимый файл макета упаковки.</span><span class="sxs-lookup"><span data-stu-id="0646b-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-548"><strong>паккажесигнконфиг</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="0646b-549">0x80080212</span></span></td>
<td><span data-ttu-id="0646b-550">Недопустимый файл Паккажесигнконфиг.</span><span class="sxs-lookup"><span data-stu-id="0646b-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="0646b-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="0646b-553">0x80080213</span></span></td>
<td><span data-ttu-id="0646b-554">Файл Resources. PRI не разрешен, если в манифесте пакета нет элементов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0646b-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="0646b-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="0646b-557">0x80080214</span></span></td>
<td><span data-ttu-id="0646b-558">Состояние сжатия файла в базовом плане и обновленный пакет не совпадают.</span><span class="sxs-lookup"><span data-stu-id="0646b-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0646b-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="0646b-561">0x80080215</span></span></td>
<td><span data-ttu-id="0646b-562">Расширения, отличные от. appx, не разрешены для пакетов полезных данных, предназначенных для старых платформ.</span><span class="sxs-lookup"><span data-stu-id="0646b-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0646b-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="0646b-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="0646b-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="0646b-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="0646b-565">0x80080216</span></span></td>
<td><span data-ttu-id="0646b-566">Недопустимый файл Енкриптионексклусионфилелист.</span><span class="sxs-lookup"><span data-stu-id="0646b-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="0646b-567">Приложения не запускаются, и их имена недоступны</span><span class="sxs-lookup"><span data-stu-id="0646b-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="0646b-568">На компьютере под управлением Windows 10 невозможно запустить некоторые приложения, и имена приложений отображаются серым цветом.</span><span class="sxs-lookup"><span data-stu-id="0646b-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Некоторые имена приложений в меню "Пуск" отображаются серым цветом](./images/app-names-dimmed.png)

<span data-ttu-id="0646b-570">При попытке открыть приложение, выбрав затененное имя, может появиться одно из следующих сообщений об ошибке:</span><span class="sxs-lookup"><span data-stu-id="0646b-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="0646b-571">Возникла проблема с \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="0646b-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="0646b-572">Обратитесь к системному администратору, чтобы восстановить или переустановить его.</span><span class="sxs-lookup"><span data-stu-id="0646b-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="0646b-573">Ошибка: это приложение не может быть открыто</span><span class="sxs-lookup"><span data-stu-id="0646b-573">Error: This app can't open</span></span>

<span data-ttu-id="0646b-574">Кроме того, следующие записи событий регистрируются в журнале "Microsoft-Windows-Твинуи/эксплуатация" в разделе " **приложения и сервицес\микрософт\виндовс\аппс**".</span><span class="sxs-lookup"><span data-stu-id="0646b-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="0646b-575">Имя журнала: Microsoft-Windows-Твинуи/эксплуатация</span><span class="sxs-lookup"><span data-stu-id="0646b-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="0646b-576">Источник: Microsoft-Windows-иммерсивное-Shell</span><span class="sxs-lookup"><span data-stu-id="0646b-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="0646b-577">Дата: <*Дата*></span><span class="sxs-lookup"><span data-stu-id="0646b-577">Date: <*date*></span></span>  
> <span data-ttu-id="0646b-578">Идентификатор события: 5960</span><span class="sxs-lookup"><span data-stu-id="0646b-578">Event ID: 5960</span></span>  
> <span data-ttu-id="0646b-579">Категория задачи: (5960)</span><span class="sxs-lookup"><span data-stu-id="0646b-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="0646b-580">Level: Error</span><span class="sxs-lookup"><span data-stu-id="0646b-580">Level: Error</span></span>  
> <span data-ttu-id="0646b-581">Ключевые слова:</span><span class="sxs-lookup"><span data-stu-id="0646b-581">Keywords:</span></span>  
> <span data-ttu-id="0646b-582">Описание.</span><span class="sxs-lookup"><span data-stu-id="0646b-582">Description:</span></span>  
> <span data-ttu-id="0646b-583">Активация приложения Microsoft.BingNews_8wekyb3d8bbwe! Аппексневс для Windows.</span><span class="sxs-lookup"><span data-stu-id="0646b-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="0646b-584">Контракт запуска заблокирован с ошибкой 0x80073CFC, так как его пакет находится в состоянии: изменен.</span><span class="sxs-lookup"><span data-stu-id="0646b-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="0646b-585">Причина</span><span class="sxs-lookup"><span data-stu-id="0646b-585">Cause</span></span>

<span data-ttu-id="0646b-586">Эта проблема возникает из-за изменения записи реестра для значения состояния соответствующего пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="0646b-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="0646b-587">Решение</span><span class="sxs-lookup"><span data-stu-id="0646b-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="0646b-588">При неправильном изменении реестра с помощью редактора реестра или иного метода могут возникнуть серьезные проблемы.</span><span class="sxs-lookup"><span data-stu-id="0646b-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="0646b-589">Эти проблемы могут потребовать переустановки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0646b-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="0646b-590">Корпорация Майкрософт не гарантирует, что такие неполадки могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="0646b-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="0646b-591">Ответственность за изменение реестра лежит на пользователе.</span><span class="sxs-lookup"><span data-stu-id="0646b-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="0646b-592">Чтобы устранить эту проблему:</span><span class="sxs-lookup"><span data-stu-id="0646b-592">To fix this issue:</span></span>

1. <span data-ttu-id="0646b-593">Откройте редактор реестра и найдите подраздел **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .</span><span class="sxs-lookup"><span data-stu-id="0646b-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="0646b-594">Чтобы создать резервную копию данных подраздела, щелкните правой кнопкой мыши **паккажелист**, выберите пункт **Экспорт**, а затем сохраните данные в виде файла реестра.</span><span class="sxs-lookup"><span data-stu-id="0646b-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="0646b-595">Для каждого из приложений, перечисленных в записях журнала Event ID 5960, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0646b-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="0646b-596">Откройте запись **паккажестатус** .</span><span class="sxs-lookup"><span data-stu-id="0646b-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="0646b-597">Установите значение **паккажестатус** равным нулю (**0**).</span><span class="sxs-lookup"><span data-stu-id="0646b-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="0646b-598">Если в **паккажелист** нет записей для приложения, значит, у проблемы есть другая причина.</span><span class="sxs-lookup"><span data-stu-id="0646b-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="0646b-599">В случае с примером события в этой статье полный подраздел — **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="0646b-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="0646b-600">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="0646b-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="0646b-601">Получите дополнительную справку</span><span class="sxs-lookup"><span data-stu-id="0646b-601">Get additional help</span></span>

<span data-ttu-id="0646b-602">Если вам нужна дополнительная помощь по устранению проблемы, которая возникает при упаковке, развертывании или запросе пакета приложения Windows (. msix/. appx) в качестве разработчика, обратитесь к этим дополнительным ресурсам поддержки для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="0646b-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="0646b-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) предоставляет актуальные и своевременные ответы на технические проблемы от сообщества экспертов и инженеров Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0646b-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="0646b-604">Для помощи в сообществе с вопросами по разработке есть наши [форумы](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)и [StackOverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="0646b-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="0646b-605">На сайте [поддержки для разработчиков Windows](https://developer.microsoft.com/windows/support) описаны другие варианты поддержки.</span><span class="sxs-lookup"><span data-stu-id="0646b-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0646b-606">См. также</span><span class="sxs-lookup"><span data-stu-id="0646b-606">Related topics</span></span>

- <span data-ttu-id="0646b-607">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Подписывание пакета приложения с помощью SignTool)</span><span class="sxs-lookup"><span data-stu-id="0646b-607">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
- [<span data-ttu-id="0646b-608">Устранение ошибок подписи пакета приложения</span><span class="sxs-lookup"><span data-stu-id="0646b-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)

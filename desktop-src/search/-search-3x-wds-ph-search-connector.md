---
description: Проводник Windows управляет созданием соединителя поиска для обработчика протокола с помощью записей разделов реестра. В реестре как разработчики, так и сторонние лица могут включать новые и устаревшие обработчики протоколов для участия в поиске Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Создание соединителя поиска для обработчика протокола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144173"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="1c998-104">Создание соединителя поиска для обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="1c998-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="1c998-105">Проводник Windows управляет созданием соединителя поиска для обработчика протокола с помощью записей разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="1c998-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="1c998-106">В реестре как разработчики, так и сторонние лица могут включать новые и устаревшие обработчики протоколов для участия в поиске Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c998-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="1c998-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c998-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1c998-108">Сведения о соединителях поиска для обработчиков протоколов в Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c998-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="1c998-109">Включение обработчиков протоколов для участия в поиске</span><span class="sxs-lookup"><span data-stu-id="1c998-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="1c998-110">Идет отключение создания соединителя поиска для обработчика протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="1c998-111">Настройка имени, описания или Фолдертипе для соединителя поиска обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="1c998-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="1c998-112">Использование перенаправления строк реестра</span><span class="sxs-lookup"><span data-stu-id="1c998-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="1c998-113">Восстановление удаленного соединителя поиска обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="1c998-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1c998-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="1c998-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1c998-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="1c998-116">Сведения о соединителях поиска для обработчиков протоколов в Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c998-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="1c998-117">В Windows 7 Поиск в меню « **Пуск** » или в проводнике Windows включает в себя только файлы в индексируемых расположениях, а также элементы нефайловой системы, такие как удаленные хранилища данных или элементы обработчика протоколов, у которых есть соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="1c998-118">В дополнение к включению элементов обработчика протоколов в области поиска в меню " **Пуск** " и "оболочка" соединитель поиска позволяет меню " **Пуск** " Группировать элементы обработчика протокола в **результатах меню "Пуск"** , в результате чего пользователь может щелкнуть заголовок группы и просмотреть результаты только из обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="1c998-119">Кроме того, пользователь может перейти в папку **Поиск** , открыть файл соединителя поиска и выполнить поиск, содержащий только элементы конкретного обработчика протокола, связанного с этим соединителем поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="1c998-120">Когда пользователь впервые запускает приложение, которое регистрирует обработчик протокола, проводник Windows создает файл соединителя поиска (. Сеарчконнектор-MS) для обработчика протокола в папке " **Поиск** " пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c998-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="1c998-121">Приложения с обработчиками протоколов могут отключить это поведение или настроить имя и описание соединителя поиска для обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="1c998-122">Расположение папки " **Поиск** " пользователя:% UserProfile% \\ операций поиска или FOLDERID \_ саведсеарчес.</span><span class="sxs-lookup"><span data-stu-id="1c998-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="1c998-123">Идентификатор GUID для FOLDERID \_ саведсеарчес — {7d1d3a04-Debb-4115-95cf-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="1c998-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="1c998-124">Проводник Windows управляет созданием соединителя поиска для обработчика протокола с помощью записей разделов реестра, описанных в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1c998-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="1c998-125">Включение обработчиков протоколов для участия в поиске</span><span class="sxs-lookup"><span data-stu-id="1c998-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="1c998-126">Идет отключение создания соединителя поиска для обработчика протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="1c998-127">Настройка имени, описания или Фолдертипе для соединителя поиска обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="1c998-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="1c998-128">Восстановление удаленного соединителя поиска обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="1c998-129">Нет программных средств для создания соединителя поиска для обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="1c998-130">Они должны быть настроены в реестре.</span><span class="sxs-lookup"><span data-stu-id="1c998-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="1c998-131">Включение обработчиков протоколов для участия в поиске</span><span class="sxs-lookup"><span data-stu-id="1c998-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="1c998-132">Разделы реестра и их возможные значения описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c998-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="1c998-133">Обработчик протокола может заполнить некоторые или все из этих разделов реестра <protocol> , где заменяется фактическим именем его протокола, например MAPI, File или CSC.</span><span class="sxs-lookup"><span data-stu-id="1c998-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="1c998-134">Раздел реестра</span><span class="sxs-lookup"><span data-stu-id="1c998-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="1c998-135">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1c998-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="1c998-136">Тип</span><span class="sxs-lookup"><span data-stu-id="1c998-136">Type</span></span>       | <span data-ttu-id="1c998-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c998-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c998-138">HKey \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Search \\ фсеарчконнекторс \\ <protocol> \\ версия</span><span class="sxs-lookup"><span data-stu-id="1c998-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="1c998-139">Не существует (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1c998-139">Does not exist (default).</span></span> <span data-ttu-id="1c998-140">В противном случае — 1 или больше.</span><span class="sxs-lookup"><span data-stu-id="1c998-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="1c998-141">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="1c998-141">REG\_DWORD</span></span> | <span data-ttu-id="1c998-142">Это значение используется для обнаружения изменений в регистрации шаблона расположения для корней поиска, которые уже были обработаны.</span><span class="sxs-lookup"><span data-stu-id="1c998-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="1c998-143">Если не существует, по умолчанию используется значение 0.</span><span class="sxs-lookup"><span data-stu-id="1c998-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="1c998-144">Кроме того, можно увеличить версию, чтобы сообщить проводнику Windows о необходимости повторного создания соединителя поиска, поскольку установлен более новая версия обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="1c998-145">HKey \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Search \\ фсеарчконнекторс \\ <protocol> \\ доноткреатесеарчконнекторс</span><span class="sxs-lookup"><span data-stu-id="1c998-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="1c998-146">Не существует (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1c998-146">Does not exist (default).</span></span> <span data-ttu-id="1c998-147">В противном случае устанавливается значение 1.</span><span class="sxs-lookup"><span data-stu-id="1c998-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="1c998-148">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="1c998-148">REG\_DWORD</span></span> | <span data-ttu-id="1c998-149">Если он не существует, создайте файл. сеарчконнектор-MS в папке поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="1c998-150">Если значение равно 1, пометьте как обработанное и не предпринимайте никаких действий.</span><span class="sxs-lookup"><span data-stu-id="1c998-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="1c998-151">HKey \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Search \\ фсеарчконнекторс \\ <protocol> \\ Описание по умолчанию \\</span><span class="sxs-lookup"><span data-stu-id="1c998-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="1c998-152">Локализуемое строка, содержащая описание соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="1c998-153">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1c998-153">REG\_SZ</span></span>    | <span data-ttu-id="1c998-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1c998-154">Optional.</span></span> <span data-ttu-id="1c998-155">Он используется в элементе Description файла сеарчконнектор-MS.</span><span class="sxs-lookup"><span data-stu-id="1c998-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1c998-156">HKey \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Search \\ фсеарчконнекторс \\ <protocol> \\ имя по умолчанию \\</span><span class="sxs-lookup"><span data-stu-id="1c998-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="1c998-157">Локализованная строка для имени соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-157">A localized string to name the search connector.</span></span> <span data-ttu-id="1c998-158">Используется в качестве имени файла сеарчконнектор-MS.</span><span class="sxs-lookup"><span data-stu-id="1c998-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="1c998-159">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1c998-159">REG\_SZ</span></span>    | <span data-ttu-id="1c998-160">Каждое расположение должно иметь уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="1c998-160">Each location must have a unique name.</span></span> <span data-ttu-id="1c998-161">При отсутствии этого значения будет использоваться отображаемое имя, предоставленное [интерфейсом ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="1c998-162">HKey \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows Search \\ фсеарчконнекторс \\ <protocol> \\ по умолчанию \\ фолдертипе</span><span class="sxs-lookup"><span data-stu-id="1c998-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="1c998-163">Идентификатор GUID, определяющий [фолдертипеид](../shell/foldertypeid.md) , применяемый к соединителю поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="1c998-164">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="1c998-164">REG\_SZ</span></span>    | <span data-ttu-id="1c998-165">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1c998-165">Optional.</span></span> <span data-ttu-id="1c998-166">Используется в элементе Фолдертипе файла сеарчконнектор-MS для указания шаблонов, которые должны использоваться для отображения результатов.</span><span class="sxs-lookup"><span data-stu-id="1c998-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="1c998-167">Например, значение идентификатора GUID для документов ФОЛДЕРТИПЕИД \_ .</span><span class="sxs-lookup"><span data-stu-id="1c998-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="1c998-168">Идет отключение создания соединителя поиска для обработчика протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="1c998-169">Если приложение предоставляет элементы через обработчик протокола для использования в самом приложении и нежелательно предоставлять эти элементы через оболочку (в меню « **Пуск** » и в проводнике Windows), необходимо отключить создание соединителя поиска для обработчика протокола.</span><span class="sxs-lookup"><span data-stu-id="1c998-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="1c998-170">Чтобы отключить создание соединителя поиска, задайте для Доноткреатесеарчконнекторс значение 0x00000001 (1), как показано в следующем примере раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="1c998-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="1c998-171">Если Доноткреатесеарчконнекторс имеет значение 1, рекомендуется предоставить свойство [System. Shell. омитфромвиев](/windows/desktop/properties/props-system-shell-omitfromview) для каждого элемента, предоставляемого обработчиком протокола, и присвоить этому свойству значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1c998-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="1c998-172">Это предотвратит отображение элементов обработчика протокола в группе **файлы** меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="1c998-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="1c998-173">Если Доноткреатесеарчконнекторс имеется и имеет значение 0, проводник Windows создаст соединитель поиска для обработчика протокола, а элементы обработчика протокола будут возвращены в меню " **Пуск** " и в результатах поиска проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="1c998-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="1c998-174">Настройка имени, описания или Фолдертипе для соединителя поиска обработчика протокола</span><span class="sxs-lookup"><span data-stu-id="1c998-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="1c998-175">Имя соединителя поиска используется не только для обнаружения соединителя поиска в папке searchs, но и для результатов поиска в **меню "** **Пуск** " в заголовке группы.</span><span class="sxs-lookup"><span data-stu-id="1c998-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="1c998-176">Поэтому важно указать описательное имя для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="1c998-177">Если в разделе реестра не указано имя, по умолчанию проводник Windows использует имя, предоставленное [интерфейсом ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , для корня поиска обработчика протокола и пустого описания.</span><span class="sxs-lookup"><span data-stu-id="1c998-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="1c998-178">Имя по умолчанию можно переопределить с помощью записи раздела реестра без необходимости переименования интерфейса Ишеллфолдер.</span><span class="sxs-lookup"><span data-stu-id="1c998-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="1c998-179">Хотя это не так видно, как имя соединителя поиска, можно также переопределить Описание соединителя поиска, предоставив собственное описание.</span><span class="sxs-lookup"><span data-stu-id="1c998-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="1c998-180">Чтобы переопределить имя или описание по умолчанию, задайте записи, как показано в следующем примере реестра.</span><span class="sxs-lookup"><span data-stu-id="1c998-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="1c998-181">Кроме того, для записи Фолдертипе можно задать один из идентификаторов GUID [фолдертипеид](../shell/foldertypeid.md) .</span><span class="sxs-lookup"><span data-stu-id="1c998-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="1c998-182">Значение должно быть фактическим идентификатором GUID, а не именем.</span><span class="sxs-lookup"><span data-stu-id="1c998-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="1c998-183">Например, {94d6ddcc-4A68-4175-a374-bd584a510b78}, а не ФОЛДЕРТИПЕИД \_ Music.</span><span class="sxs-lookup"><span data-stu-id="1c998-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="1c998-184">Идентификатор GUID для ФОЛДЕРТИПЕИД можно получить в файле заголовка Шлгуид. h в [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c998-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="1c998-185">Использование перенаправления строк реестра</span><span class="sxs-lookup"><span data-stu-id="1c998-185">Using Registry String Redirection</span></span>

<span data-ttu-id="1c998-186">Можно использовать [перенаправленную строку](../intl/using-registry-string-redirection.md) , чтобы обеспечить локализацию имени, которое вы хотите указать для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="1c998-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="1c998-187">Можно включить локализуемые строки в разделы реестра Name и Description вместо того, чтобы вводить фактическую строку в реестр.</span><span class="sxs-lookup"><span data-stu-id="1c998-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="1c998-188">Чтобы включить локализуемое строку для значений имени или описания, задайте значение, как показано в следующем примере раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="1c998-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="1c998-189">Локализуемое строка имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="1c998-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="1c998-190">@dllname.dll,-resourceID, где:</span><span class="sxs-lookup"><span data-stu-id="1c998-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="1c998-191">@dllname.dll путь к библиотеке DLL, содержащей строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="1c998-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="1c998-192">resourceID — это целочисленный идентификатор ресурса строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="1c998-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="1c998-193">Формат косвенной строки и косвенная строка, добавленная с помощью модификатора версии, описаны в [функции шлоадиндиректстринг](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="1c998-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="1c998-194">Восстановление удаленного соединителя поиска обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="1c998-195">Так как соединители поиска являются файлами на компьютере пользователя, они могут быть удалены по ошибке.</span><span class="sxs-lookup"><span data-stu-id="1c998-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="1c998-196">Чтобы восстановить все соединители поиска удаленных обработчиков протоколов, восстановите библиотеки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c998-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="1c998-197">Для этого откройте проводник Windows, щелкните правой кнопкой мыши папку **библиотеки** и выберите **восстановить библиотеки по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="1c998-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![снимок экрана с командой меню "восстановить библиотеки по умолчанию"](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="1c998-199">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1c998-199">Additional Resources</span></span>

-   [<span data-ttu-id="1c998-200">Интерфейса IShellItem::/DisplayName</span><span class="sxs-lookup"><span data-stu-id="1c998-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="1c998-201">СИГДН \_ нормалдисплай</span><span class="sxs-lookup"><span data-stu-id="1c998-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="1c998-202">См. также</span><span class="sxs-lookup"><span data-stu-id="1c998-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1c998-203">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1c998-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1c998-204">Основные сведения о обработчиках протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="1c998-205">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="1c998-206">Уведомление индекса изменений</span><span class="sxs-lookup"><span data-stu-id="1c998-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="1c998-207">Добавление значков и контекстных меню</span><span class="sxs-lookup"><span data-stu-id="1c998-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="1c998-208">Пример кода: расширения оболочки для обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="1c998-209">Установка и регистрация обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="1c998-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="1c998-210">Обработчики протокола отладки</span><span class="sxs-lookup"><span data-stu-id="1c998-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

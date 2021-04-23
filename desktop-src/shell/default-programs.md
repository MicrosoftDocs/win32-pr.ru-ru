---
description: Используйте программы по умолчанию, чтобы задать пользовательский интерфейс по умолчанию.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Программы по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2021
ms.locfileid: "103913911"
---
# <a name="default-programs"></a><span data-ttu-id="800ff-103">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-103">Default Programs</span></span>

<span data-ttu-id="800ff-104">Используйте **программы по умолчанию** , чтобы задать пользовательский интерфейс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="800ff-105">Пользователи могут получить доступ к **программам по умолчанию** из панели управления или непосредственно из меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="800ff-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="800ff-106">[Установка средства доступа к программам и параметров по умолчанию (SPAD)](cpl-setprogramaccess.md) . Основные параметры по умолчанию для пользователей в Windows XP теперь представляют собой одну часть **программ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="800ff-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="800ff-107">Этот раздел не относится к Windows 10.</span><span class="sxs-lookup"><span data-stu-id="800ff-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="800ff-108">Способ изменения связей файлов по умолчанию в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="800ff-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="800ff-109">Дополнительные сведения см. в разделе об **изменениях в статье обработка приложений по умолчанию** в [этой записи](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="800ff-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="800ff-110">Когда пользователь устанавливает параметры программы по умолчанию при помощи **программ по умолчанию**, параметр по умолчанию применяется только к этому пользователю, а не к другим пользователям, которые могут использовать тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="800ff-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="800ff-111">**Программы по умолчанию** предоставляют набор интерфейсов API (не рекомендуется в Windows 8), которые позволяют независимым поставщикам программного обеспечения включать свои программы или приложения в систему по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="800ff-112">Набор API также помогает поставщикам программного обеспечения лучше управлять своим состоянием по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="800ff-113">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="800ff-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="800ff-114">Общие сведения о программах по умолчанию и связанном наборе API</span><span class="sxs-lookup"><span data-stu-id="800ff-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="800ff-115">Регистрация приложения для использования с программами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="800ff-116">Идентификаторы ProgID</span><span class="sxs-lookup"><span data-stu-id="800ff-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="800ff-117">Описание подраздела и значения регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="800ff-118">регистередаппликатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="800ff-119">Пример полной регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="800ff-120">Становится браузером по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="800ff-121">Пользовательский интерфейс программ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="800ff-122">Рекомендации по использованию программ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="800ff-123">Во время установки</span><span class="sxs-lookup"><span data-stu-id="800ff-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="800ff-124">После установки</span><span class="sxs-lookup"><span data-stu-id="800ff-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="800ff-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="800ff-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="800ff-126">См. также</span><span class="sxs-lookup"><span data-stu-id="800ff-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="800ff-127">Общие сведения о программах по умолчанию и связанном наборе API</span><span class="sxs-lookup"><span data-stu-id="800ff-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="800ff-128">**Программы по умолчанию** в основном предназначены для приложений, использующих стандартные типы файлов, такие как MP3-или JPG-файлы или стандартные протоколы, такие как HTTP или mailto.</span><span class="sxs-lookup"><span data-stu-id="800ff-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="800ff-129">Приложения, использующие собственные собственные протоколы и сопоставления файлов, обычно не используют функциональные возможности **программ по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="800ff-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="800ff-130">После регистрации приложения для работы с **программами по умолчанию** доступны следующие параметры и функциональные возможности с помощью набора API:</span><span class="sxs-lookup"><span data-stu-id="800ff-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="800ff-131">Восстановить все зарегистрированные значения по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="800ff-132">Не рекомендуется для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="800ff-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="800ff-133">Восстановление одного зарегистрированного значения по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="800ff-134">Не рекомендуется для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="800ff-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="800ff-135">Запрос владельца конкретного значения по умолчанию в одном вызове вместо поиска в реестре.</span><span class="sxs-lookup"><span data-stu-id="800ff-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="800ff-136">Можно запросить значение по умолчанию для канонического глагола сопоставления файлов, протокола или меню **запуска** .</span><span class="sxs-lookup"><span data-stu-id="800ff-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="800ff-137">Запуск пользовательского интерфейса для конкретного приложения, в котором пользователь может задать индивидуальные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="800ff-138">Удалите все связи для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-138">Remove all per-user associations.</span></span>

<span data-ttu-id="800ff-139">**Программы по умолчанию** также предоставляют пользовательский интерфейс, позволяющий зарегистрировать приложение, чтобы предоставить пользователю дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="800ff-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="800ff-140">Например, приложение с цифровой подписью может включать URL-адрес домашней страницы изготовителя.</span><span class="sxs-lookup"><span data-stu-id="800ff-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="800ff-141">Использование соответствующего набора API может помочь в правильной работе приложения в функции контроля учетных записей (UAC), появившейся в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="800ff-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="800ff-142">Под контролем учетных записей администратор выводит систему в качестве обычного пользователя, поэтому администратор не может обычно выполнять запись в поддерево " **\_ локальный \_ компьютер" hKey** .</span><span class="sxs-lookup"><span data-stu-id="800ff-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="800ff-143">Это ограничение является функцией безопасности, которая не позволяет процессу выступать в качестве администратора без ведома администратора.</span><span class="sxs-lookup"><span data-stu-id="800ff-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="800ff-144">Установка программы пользователем обычно выполняется в виде процесса с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="800ff-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="800ff-145">Однако попытки приложения изменить поведение связи по умолчанию на уровне компьютера после установки не будут успешными.</span><span class="sxs-lookup"><span data-stu-id="800ff-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="800ff-146">Вместо этого значения по умолчанию должны быть зарегистрированы на уровне отдельных пользователей, что не позволяет нескольким пользователям перезаписывать значения по умолчанию для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="800ff-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="800ff-147">Иерархическая структура реестра для сопоставлений файлов и протоколов обеспечивает приоритет для параметров по умолчанию на уровне компьютера для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="800ff-148">Некоторые приложения включают в себя точки кода, которые временно расширяют свои права при утверждении значений по умолчанию, зарегистрированных на **\_ локальном \_ компьютере hKey**.</span><span class="sxs-lookup"><span data-stu-id="800ff-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="800ff-149">Эти приложения могут столкнуться с непредвиденными результатами, если другое приложение уже зарегистрировано как значение по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="800ff-150">Использование **программ по умолчанию** предотвращает эту неоднозначность и гарантирует ожидаемые результаты на уровне отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="800ff-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="800ff-151">Регистрация приложения для использования с программами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="800ff-152">В этом разделе показаны подразделы и значения реестра, необходимые для регистрации приложения в **программах по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="800ff-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="800ff-153">Он включает полный пример.</span><span class="sxs-lookup"><span data-stu-id="800ff-153">It includes a full example.</span></span>

<span data-ttu-id="800ff-154">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="800ff-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="800ff-155">Идентификаторы ProgID</span><span class="sxs-lookup"><span data-stu-id="800ff-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="800ff-156">Описание подраздела и значения регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="800ff-157">регистередаппликатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="800ff-158">Пример полной регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="800ff-159">**Программы по умолчанию** требуют, чтобы каждое приложение регистрировало явные сопоставления файлов, сопоставления MIME и протоколы, для которых приложение должно быть указано как возможное по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="800ff-160">Вы регистрируете связи с помощью следующих элементов реестра, которые подробно описаны далее в разделе [подраздел регистрации и описание значения](#registration-subkey-and-value-descriptions).</span><span class="sxs-lookup"><span data-stu-id="800ff-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="800ff-161">В следующем примере показаны записи реестра для вымышленного браузера Contoso, который называется WebBrowser:</span><span class="sxs-lookup"><span data-stu-id="800ff-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="800ff-162">Идентификаторы ProgID</span><span class="sxs-lookup"><span data-stu-id="800ff-162">ProgIDs</span></span>

<span data-ttu-id="800ff-163">Приложение должно предоставить конкретный [идентификатор ProgID](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="800ff-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="800ff-164">Не забудьте включить все сведения, которые обычно записываются в общий подраздел по умолчанию для расширения.</span><span class="sxs-lookup"><span data-stu-id="800ff-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="800ff-165">Например, вымышленный проигрыватель мультимедиа Litware содержит классы программного обеспечения файла **hKey \_ локального \_ компьютера** для конкретного приложения \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** подраздела.</span><span class="sxs-lookup"><span data-stu-id="800ff-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="800ff-166">Этот подраздел включает все сведения в общем подразделе по умолчанию **hKey Software \_ \_ Machine** \\  \\ **Classes** \\ **. mp3** , а также дополнительные сведения, которые требуется зарегистрировать в приложении.</span><span class="sxs-lookup"><span data-stu-id="800ff-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="800ff-167">Это гарантирует, что если пользователь восстановит связь. mp3 с проигрывателем Litware, сведения о проигрывателе Litware не будут изменены и не будут перезаписаны другим приложением.</span><span class="sxs-lookup"><span data-stu-id="800ff-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="800ff-168">(Перезапись может произойти, если подразделом по умолчанию является единственным источником этой информации.)</span><span class="sxs-lookup"><span data-stu-id="800ff-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="800ff-169">При сопоставлении ProgID с расширением или протоколом имени файла приложение может сопоставлять "один к одному" или "один ко многим".</span><span class="sxs-lookup"><span data-stu-id="800ff-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="800ff-170">В примере Contoso Контосохтмл указывает на один идентификатор ProgID, предоставляющий сведения о ShellExecute для расширений. htm,. HTML,. shtml,. ксхт и. XHTML.</span><span class="sxs-lookup"><span data-stu-id="800ff-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="800ff-171">Поскольку для каждого протокола существует другой идентификатор ProgID, при использовании протоколов каждый протокол включает свою собственную строку выполнения.</span><span class="sxs-lookup"><span data-stu-id="800ff-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="800ff-172">Если тип MIME можно просмотреть в браузере, ProgID для типа MIME должен содержать подраздел **CLSID** , который использует идентификатор класса (CLSID) соответствующего приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="800ff-173">Этот идентификатор CLSID используется в уточняющем запросе к идентификатору CLSID в базе данных MIME, который хранится в списке класс программного обеспечения для **\_ локального \_ компьютера hKey** \\  \\  \\  \\  \\ **тип содержимого** базы данных MIME.</span><span class="sxs-lookup"><span data-stu-id="800ff-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="800ff-174">Если тип MIME не предназначен для просмотра в браузере, этот шаг можно опустить.</span><span class="sxs-lookup"><span data-stu-id="800ff-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="800ff-175">Описание подраздела и значения регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="800ff-176">В этом разделе описаны отдельные подразделы и значения реестра, используемые при регистрации приложения с **программами по умолчанию**, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="800ff-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="800ff-177">Характеристики</span><span class="sxs-lookup"><span data-stu-id="800ff-177">Capabilities</span></span>

<span data-ttu-id="800ff-178">Подраздел **возможностей** содержит все сведения о **программах по умолчанию** для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="800ff-179">Заполнитель% Аппликатионкапабилитипас% относится к пути реестра из раздела **hKey \_ текущий \_ пользователь** или **hKey \_ локальный \_ компьютер** к подразделу **возможностей** приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="800ff-180">Этот подраздел содержит важные значения, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="800ff-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="800ff-181">Значение</span><span class="sxs-lookup"><span data-stu-id="800ff-181">Value</span></span>                  | <span data-ttu-id="800ff-182">Тип</span><span class="sxs-lookup"><span data-stu-id="800ff-182">Type</span></span>                       | <span data-ttu-id="800ff-183">Значение</span><span class="sxs-lookup"><span data-stu-id="800ff-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800ff-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="800ff-184">ApplicationDescription</span></span> | <span data-ttu-id="800ff-185">REG \_ SZ или REG \_ expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="800ff-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="800ff-186">**Обязательно**.</span><span class="sxs-lookup"><span data-stu-id="800ff-186">**Required**.</span></span> <span data-ttu-id="800ff-187">Чтобы разрешить пользователю принимать информированное назначение по умолчанию, приложение должно предоставить строку, описывающую возможности приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="800ff-188">Хотя предыдущий пример Contoso присваивает описание непосредственно значению Аппликатиондескриптион, приложения обычно предоставляют описание в виде ресурса, внедренного в DLL-файл для упрощения локализации.</span><span class="sxs-lookup"><span data-stu-id="800ff-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="800ff-189">Если Аппликатиондескриптион не указан, приложение не отображается в списках пользовательского интерфейса потенциальных программ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="800ff-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="800ff-190">ApplicationName</span></span>        | <span data-ttu-id="800ff-191">REG \_ SZ или REG \_ expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="800ff-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="800ff-192">**Необязательный элемент.**</span><span class="sxs-lookup"><span data-stu-id="800ff-192">**Optional.**</span></span> <span data-ttu-id="800ff-193">Имя, по которому программа отображается в пользовательском интерфейсе программы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="800ff-194">Если эти данные не предоставляются приложением, имя исполняемой программы, связанной с первым зарегистрированным ProgID для приложения, используется в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="800ff-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="800ff-195">Имя ApplicationName должно всегда совпадать с именем, зарегистрированным в [регистередаппликатионс](#registeredapplications).</span><span class="sxs-lookup"><span data-stu-id="800ff-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="800ff-196">Вы можете использовать ApplicationName, если хотите, чтобы различные типы приложений, например браузер и почтовый клиент, указывали на один и тот же исполняемый файл, когда они отображаются с разными именами.</span><span class="sxs-lookup"><span data-stu-id="800ff-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="800ff-197">Скрытый</span><span class="sxs-lookup"><span data-stu-id="800ff-197">Hidden</span></span>                 | <span data-ttu-id="800ff-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="800ff-198">REG\_DWORD</span></span>                 | <span data-ttu-id="800ff-199">**Необязательный элемент.**</span><span class="sxs-lookup"><span data-stu-id="800ff-199">**Optional.**</span></span> <span data-ttu-id="800ff-200">Установите значение 1, чтобы отключить приложение из списка программ диалогового окна **Настройка программ по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="800ff-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="800ff-201">Если это значение равно 0 или отсутствует, приложение отображается в списке в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="800ff-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="800ff-202">филеассоЦиатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-202">FileAssociations</span></span>

<span data-ttu-id="800ff-203">Подраздел **филеассоЦиатионс** содержит определенные сопоставления файлов, затребованные приложением.</span><span class="sxs-lookup"><span data-stu-id="800ff-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="800ff-204">Эти утверждения хранятся в виде значений с одним значением для каждого расширения.</span><span class="sxs-lookup"><span data-stu-id="800ff-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="800ff-205">Ассоциации указывают на ProgID конкретного приложения вместо универсального ProgID.</span><span class="sxs-lookup"><span data-stu-id="800ff-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="800ff-206">Однако все ассоциации не обязательно должны указывать на один и тот же идентификатор ProgID.</span><span class="sxs-lookup"><span data-stu-id="800ff-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="800ff-207">мимеассоЦиатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-207">MIMEAssociations</span></span>

<span data-ttu-id="800ff-208">Подраздел **мимеассоЦиатионс** содержит определенные типы MIME, затребованные приложением.</span><span class="sxs-lookup"><span data-stu-id="800ff-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="800ff-209">Эти утверждения хранятся в виде значений с одним значением для каждого типа MIME.</span><span class="sxs-lookup"><span data-stu-id="800ff-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="800ff-210">Имя значения для каждого типа MIME должно точно совпадать с именем MIME, хранящимся в базе данных MIME.</span><span class="sxs-lookup"><span data-stu-id="800ff-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="800ff-211">Этому значению также необходимо назначить идентификатор ProgID для конкретного приложения, который содержит соответствующий идентификатор CLSID приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="800ff-212">Связывается</span><span class="sxs-lookup"><span data-stu-id="800ff-212">Startmenu</span></span>

<span data-ttu-id="800ff-213">Подраздел **связывается** связан с назначенными пользователем записями **Интернета** и **электронной почты** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="800ff-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="800ff-214">Приложение должно быть зарегистрировано отдельно в качестве средства для этих записей.</span><span class="sxs-lookup"><span data-stu-id="800ff-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="800ff-215">Дополнительные сведения см. в разделе [Регистрация программ с помощью типов клиентов](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="800ff-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="800ff-216">Начиная с Windows 7, в меню " **Пуск** " больше нет записей **Интернета** и **электронной почты** .</span><span class="sxs-lookup"><span data-stu-id="800ff-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="800ff-217">Данные реестра, связанные с записью **электронной почты** , по-прежнему используются для клиента MAPI по умолчанию, но данные реестра, связанные с записью в **Интернете** , не используются в Windows.</span><span class="sxs-lookup"><span data-stu-id="800ff-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="800ff-218">Связав регистрацию меню " **Пуск** " приложения с регистрацией **программ по умолчанию** , приложение отображается как потенциальное значение по умолчанию в пользовательском интерфейсе " **сопоставление наборов** ".</span><span class="sxs-lookup"><span data-stu-id="800ff-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="800ff-219">Если пользователь выбрал приложение в качестве значения по умолчанию и затем восстановит все значения по умолчанию для всех приложений позже, приложение будет восстановлено до своего расположения в меню " **Пуск** " для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="800ff-220">Дополнительные сведения и иллюстрация см. в разделе [Пользовательский интерфейс программ по умолчанию](#default-programs-ui) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="800ff-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="800ff-221">Подраздел **связывается** содержит две записи: Стартменуинтернет и Mail, которые соответствуют каноническим положениям **Интернета** и **электронной почты** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="800ff-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="800ff-222">Приложению назначается значение стартменуинтернет или mail, равное имени зарегистрированного подраздела приложения в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **стартменуинтернет** или **hKey Software \_ \_ Machine** Client \\ **по** \\  \\ **mail** (как описано в разделе [Регистрация программ с типами клиентов](reg-middleware-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="800ff-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="800ff-223">В случае канонического расположения **сообщения электронной почты** в меню " **Пуск** " оно представляет собой клиент MAPI по умолчанию и, таким образом, ПРЕДПОЛАГАЕТ возможность передачи вызовов MAPI.</span><span class="sxs-lookup"><span data-stu-id="800ff-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="800ff-224">В Windows 7 Этот подраздел будет использоваться для клиента MAPI по умолчанию, хотя в меню " **Пуск** " больше не существует канонического места по **электронной почте** .</span><span class="sxs-lookup"><span data-stu-id="800ff-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="800ff-225">Приложение, которое запросит значение по умолчанию для почты, должно быть зарегистрировано как обработчик MAPI в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="800ff-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="800ff-226">Если почтовый клиент не поддерживает MAPI, но по-прежнему хочет конкурировать за каноническое расположение **электронной почты** в меню " **Пуск** ", он может зарегистрировать командную строку в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="800ff-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="800ff-227">Кроме того, в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **mail** \\ *каноникалнаме* добавьте значение по умолчанию с именем приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="800ff-228">Эти записи позволяют запускать приложение из расположения **электронной почты** в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="800ff-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="800ff-229">Обратите внимание, что вызовы MAPI по-прежнему выполняются в приложении и либо переходят к предыдущему обработчику MAPI, либо завершаются ошибкой, если не задан обработчик MAPI.</span><span class="sxs-lookup"><span data-stu-id="800ff-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="800ff-230">Дополнительные сведения см. в разделе [Регистрация программ с помощью типов клиентов](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="800ff-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="800ff-231">урлассоЦиатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-231">UrlAssociations</span></span>

<span data-ttu-id="800ff-232">Подраздел **урлассоЦиатионс** содержит конкретные протоколы URL-адресов, затребованные приложением.</span><span class="sxs-lookup"><span data-stu-id="800ff-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="800ff-233">Эти утверждения хранятся в виде значений, по одному значению для каждого протокола.</span><span class="sxs-lookup"><span data-stu-id="800ff-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="800ff-234">Каждый протокол должен указывать на ProgID, зависящий от приложения, а не на универсальный идентификатор ProgID.</span><span class="sxs-lookup"><span data-stu-id="800ff-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="800ff-235">Как упоминалось в примере Contoso, можно использовать другой идентификатор ProgID для каждого протокола, чтобы каждый из них имел собственную строку выполнения.</span><span class="sxs-lookup"><span data-stu-id="800ff-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="800ff-236">регистередаппликатионс</span><span class="sxs-lookup"><span data-stu-id="800ff-236">RegisteredApplications</span></span>

<span data-ttu-id="800ff-237">Полный подраздел для **регистередаппликатионс** :</span><span class="sxs-lookup"><span data-stu-id="800ff-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="800ff-238">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **регистередаппликатионс**</span><span class="sxs-lookup"><span data-stu-id="800ff-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="800ff-239">Этот подраздел содержит операционную систему, в которой в реестре содержатся сведения о **программах по умолчанию** для приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="800ff-240">Расположение хранится в виде значения, имя которого должно совпадать с именем приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="800ff-241">Пример полной регистрации</span><span class="sxs-lookup"><span data-stu-id="800ff-241">Full Registration Example</span></span>

<span data-ttu-id="800ff-242">В этом примере показаны подразделы и значения, используемые при регистрации вымышленного проигрывателя Litware мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="800ff-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="800ff-243">Пример включает записи ProgID для того, чтобы продемонстрировать, как все они объединяются.</span><span class="sxs-lookup"><span data-stu-id="800ff-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="800ff-244">В следующем подразделе показан идентификатор ProgID для конкретного приложения для типа MIME формата. mp3:</span><span class="sxs-lookup"><span data-stu-id="800ff-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="800ff-245">Далее следует зависящий от приложения идентификатор ProgID, связывающий программу Litware с расширением имени файла. mp3.</span><span class="sxs-lookup"><span data-stu-id="800ff-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="800ff-246">Следующие записи показывают Объединенный ProgID для типа MIME формата. MPEG и расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="800ff-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="800ff-247">Следующие записи регистрируют программу Litware в **программах по умолчанию** и используют ранее зарегистрированные идентификаторы ProgID.</span><span class="sxs-lookup"><span data-stu-id="800ff-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="800ff-248">Наконец, в этом примере регистрируется расположение регистрации программ Litware **по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="800ff-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="800ff-249">Становится браузером по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-249">Becoming the Default Browser</span></span>

<span data-ttu-id="800ff-250">Регистрация в браузере должна соответствовать рекомендациям, описанным в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="800ff-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="800ff-251">После установки браузера Windows может предоставить пользователю системное уведомление, в котором пользователь может выбрать браузер в качестве системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="800ff-252">Это уведомление отображается при соблюдении следующих условий:</span><span class="sxs-lookup"><span data-stu-id="800ff-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="800ff-253">Установщик браузера вызывает [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) с флагом **шкне \_ Ассокчанжед** , чтобы сообщить Windows о регистрации новых обработчиков протоколов.</span><span class="sxs-lookup"><span data-stu-id="800ff-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="800ff-254">Windows обнаруживает, что одно или несколько новых приложений зарегистрированы для поддержки протоколов http://и https://, и пользователь еще не уведомлен.</span><span class="sxs-lookup"><span data-stu-id="800ff-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="800ff-255">Иными словами, ни один из следующих элементов не отображается для пользователя: Системное уведомление, содержащее приложение, всплывающее окно Опенвис с приложением или страница панели управления Настройка пользовательских значений по умолчанию (суд) для приложения.</span><span class="sxs-lookup"><span data-stu-id="800ff-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="800ff-256">В следующем примере показан рекомендуемый код регистрации, который установщик браузера должен запустить после записи разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="800ff-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="800ff-257">[**Шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) сначала уведомляет систему о том, что доступны новые варианты связи.</span><span class="sxs-lookup"><span data-stu-id="800ff-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="800ff-258">Вызов **шчанженотифи** необходим для обеспечения правильной работы системных параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="800ff-259">Затем инструкция [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) позволяет системным процессам обрабатывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="800ff-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="800ff-260">Если пользователь отменяет или игнорирует полученное уведомление или всплывающее окно без выбора нового браузера по умолчанию, браузер по умолчанию остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="800ff-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="800ff-261">Обратите внимание, что пользователь также может изменить браузер по умолчанию в любое время с помощью других механизмов, включая установку параметров пользователя по умолчанию на панели управления.</span><span class="sxs-lookup"><span data-stu-id="800ff-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="800ff-262">Пользовательский интерфейс программ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-262">Default Programs UI</span></span>

<span data-ttu-id="800ff-263">На иллюстрациях в этом разделе показан пользовательский интерфейс для **программ по умолчанию** , видимый пользователю.</span><span class="sxs-lookup"><span data-stu-id="800ff-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="800ff-264">На следующем рисунке показано окно основные **программы по умолчанию** в панели управления.</span><span class="sxs-lookup"><span data-stu-id="800ff-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![снимок экрана со страницей записи программ по умолчанию](images/defaultprogramsmain.png)

<span data-ttu-id="800ff-266">Когда пользователь выбирает параметр **задать программы по умолчанию** , появляется следующее окно.</span><span class="sxs-lookup"><span data-stu-id="800ff-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="800ff-267">Пользователи могут использовать эту страницу для назначения программы по умолчанию для всех типов файлов и протоколов, для которых программа является возможной по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="800ff-268">Как показано на следующем рисунке, все [зарегистрированные](#registering-an-application-for-use-with-default-programs) программы и значок программы отображаются в окне **программы** слева.</span><span class="sxs-lookup"><span data-stu-id="800ff-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![снимок экрана со страницей "Установка программ по умолчанию"](images/setyourdefaultprograms.png)

<span data-ttu-id="800ff-270">Когда пользователь выбирает программу из списка, отображаются значок программы и поставщик.</span><span class="sxs-lookup"><span data-stu-id="800ff-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="800ff-271">Если URL-адрес внедрен в сертификат программы с цифровой подписью, программа также может отобразить URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="800ff-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="800ff-272">Программы, не имеющие цифровой подписи, не могут отображать URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="800ff-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="800ff-273">Также отображается описательный текст, который предоставляется программой во время регистрации.</span><span class="sxs-lookup"><span data-stu-id="800ff-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="800ff-274">Этот текст является обязательным.</span><span class="sxs-lookup"><span data-stu-id="800ff-274">This text is required.</span></span> <span data-ttu-id="800ff-275">Под полем Описание можно определить, сколько значений по умолчанию в настоящий момент назначено программе в полном количестве, зарегистрированном для работы.</span><span class="sxs-lookup"><span data-stu-id="800ff-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="800ff-276">Чтобы назначить или восстановить программу по умолчанию для всех файлов и протоколов, для которых она зарегистрирована, пользователь нажимает кнопку **установить эту программу в качестве параметра по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="800ff-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="800ff-277">Чтобы назначить программе отдельные типы файлов и протоколы, пользователь нажимает кнопку **выбрать значения по умолчанию для этой программы** , которая отображает **набор ассоциаций для окна программы** , как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="800ff-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="800ff-278">Мы рекомендуем вызывать **связи Set для программы** с помощью [**ИаппликатионассоЦиатионрегистратионуи:: лаунчадванцедассоЦиатионуи**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span><span class="sxs-lookup"><span data-stu-id="800ff-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![снимок экрана со страницей "Задание сопоставлений" для программы](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="800ff-280">Рекомендации по использованию программ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="800ff-281">В этом разделе приводятся рекомендации по использованию **программ по умолчанию** при регистрации приложений.</span><span class="sxs-lookup"><span data-stu-id="800ff-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="800ff-282">Он также предлагает предложения по проектированию для создания приложения, предоставляющего пользователям оптимальную функциональность **программ по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="800ff-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="800ff-283">Во время установки</span><span class="sxs-lookup"><span data-stu-id="800ff-283">During Installation</span></span>

<span data-ttu-id="800ff-284">В дополнение к обычным процедурам установки в Windows XP, приложение на базе Windows Vista или более поздней версии должно быть зарегистрировано в компоненте « **программы по умолчанию** », чтобы воспользоваться преимуществами его функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="800ff-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="800ff-285">Выполните следующую последовательность действий во время установки.</span><span class="sxs-lookup"><span data-stu-id="800ff-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="800ff-286">Шаги 1-3 соответствуют действиям, которые использовались в Windows XP; Шаг 4 был впервые использован в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="800ff-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="800ff-287">Установите необходимые двоичные файлы.</span><span class="sxs-lookup"><span data-stu-id="800ff-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="800ff-288">Запись идентификаторов ProgID на \_ локальный \_ компьютер hKey.</span><span class="sxs-lookup"><span data-stu-id="800ff-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="800ff-289">Обратите внимание, что приложения должны создавать идентификаторы ProgID для конкретных приложений для своих взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="800ff-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="800ff-290">Зарегистрируйте приложение в **программах по умолчанию** , как описано выше в статьи [Регистрация приложения для использования с программами по умолчанию](#registering-an-application-for-use-with-default-programs).</span><span class="sxs-lookup"><span data-stu-id="800ff-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="800ff-291">После установки</span><span class="sxs-lookup"><span data-stu-id="800ff-291">After Installation</span></span>

<span data-ttu-id="800ff-292">В этом разделе описывается, как запрос приложения должен сначала предоставить каждому пользователю параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="800ff-293">В нем также обсуждается, как приложение может отслеживать состояние по умолчанию для возможных связей и протоколов.</span><span class="sxs-lookup"><span data-stu-id="800ff-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="800ff-294">Интерфейсы первого запуска</span><span class="sxs-lookup"><span data-stu-id="800ff-294">First Run Experiences</span></span>

<span data-ttu-id="800ff-295">При первом запуске приложения пользователем рекомендуется, чтобы в приложении отображался пользовательский интерфейс, который обычно включает следующие два варианта:</span><span class="sxs-lookup"><span data-stu-id="800ff-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="800ff-296">Примите параметры приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-296">Accept the default application settings.</span></span> <span data-ttu-id="800ff-297">Этот параметр установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-297">This option is selected by default.</span></span>
-   <span data-ttu-id="800ff-298">Настройка параметров приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-298">Customize the default application settings.</span></span>

<span data-ttu-id="800ff-299">До Windows 8, если пользователь принимает параметры по умолчанию, приложение вызывает [**иаппликатионассоЦиатионрегистратион:: сетаппасдефаулталл**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), которое преобразует все ассоциации уровня компьютера, объявленные во время установки, в параметры для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="800ff-300">Если пользователь решает настроить параметры, приложение вызывает [**иаппликатионассоЦиатионрегистратионуи:: лаунчадванцедассоЦиатионуи**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) , чтобы отобразить пользовательский интерфейс сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="800ff-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="800ff-301">На следующем рисунке показано это окно для вымышленного проигрывателя Litware мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="800ff-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![снимок экрана "Задание сопоставлений для страницы программы для Litware"](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="800ff-303">В окне Сопоставление файлов отображаются значения по умолчанию, зарегистрированные приложением, а также текущее значение по умолчанию для других расширений и протоколов.</span><span class="sxs-lookup"><span data-stu-id="800ff-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="800ff-304">После того как пользователь закончит настройку значений по умолчанию, они нажимайте кнопку **сохранить** для фиксации изменений.</span><span class="sxs-lookup"><span data-stu-id="800ff-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="800ff-305">Если пользователь нажимает кнопку **Отмена**, окно закрывается без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="800ff-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="800ff-306">Этот пользовательский интерфейс следует использовать для приложений вместо создания собственных.</span><span class="sxs-lookup"><span data-stu-id="800ff-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="800ff-307">Это позволит сохранить ресурсы, которые ранее были необходимы для разработки пользовательского интерфейса сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="800ff-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="800ff-308">Также гарантируется, что связи будут сохранены правильно.</span><span class="sxs-lookup"><span data-stu-id="800ff-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="800ff-309">Настройка приложения для проверки того, является ли оно значением по умолчанию</span><span class="sxs-lookup"><span data-stu-id="800ff-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="800ff-310">Она больше не поддерживается в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="800ff-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="800ff-311">Обычно приложения проверяют, заданы ли они по умолчанию при запуске.</span><span class="sxs-lookup"><span data-stu-id="800ff-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="800ff-312">Настройте приложения для выполнения этой проверки, вызвав [**иаппликатионассоЦиатионрегистратион:: куеряпписдефаулт**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) или [**ИаппликатионассоЦиатионрегистратион:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span><span class="sxs-lookup"><span data-stu-id="800ff-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="800ff-313">Если приложение определяет, что оно не является значением по умолчанию, оно может представлять пользовательский интерфейс, запрашивающий пользователя, следует ли принять текущую ситуацию или сделать приложение используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="800ff-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="800ff-314">Всегда включайте в этот пользовательский интерфейс флажок, который выбирается по умолчанию и предоставляет возможность не запрашивать снова.</span><span class="sxs-lookup"><span data-stu-id="800ff-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="800ff-315">Вариант по умолчанию должен быть управляемым пользователем.</span><span class="sxs-lookup"><span data-stu-id="800ff-315">The choice of default should be user driven.</span></span> <span data-ttu-id="800ff-316">Приложение не должно восстанавливаться по умолчанию без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="800ff-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="800ff-317">На следующем рисунке показан пример диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="800ff-317">The following illustration shows an example dialog box.</span></span>

![снимок экрана с примером диалогового окна](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="800ff-319">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="800ff-319">Additional Resources</span></span>

-   [<span data-ttu-id="800ff-320">**иаппликатионассоЦиатионрегистратион**</span><span class="sxs-lookup"><span data-stu-id="800ff-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="800ff-321">**иаппликатионассоЦиатионрегистратионуи**</span><span class="sxs-lookup"><span data-stu-id="800ff-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="800ff-322">См. также</span><span class="sxs-lookup"><span data-stu-id="800ff-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="800ff-323">Рекомендации по сопоставлению файлов</span><span class="sxs-lookup"><span data-stu-id="800ff-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="800ff-324">Пример сценария сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="800ff-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="800ff-325">Рекомендации по управлению приложениями по умолчанию в Windows Vista и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="800ff-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="800ff-326">Настройка доступа к программе и параметров по умолчанию для компьютера (SPAD)</span><span class="sxs-lookup"><span data-stu-id="800ff-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 

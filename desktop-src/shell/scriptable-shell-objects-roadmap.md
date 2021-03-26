---
description: Оболочка Windows предоставляет мощный набор объектов автоматизации, позволяющих программировать оболочку с помощью Microsoft Visual Basic и языков сценариев, таких как Microsoft JScript (совместимы с ECMA 262 языка) и Microsoft Visual Basic Scripting Edition (VBScript). Эти объекты можно использовать для доступа ко многим функциям и диалоговым окнам оболочки. Например, можно получить доступ к файловой системе, запустить программы и изменить параметры системы.
title: Объекты оболочки с скриптами
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985893"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="2d38e-105">Объекты оболочки с скриптами</span><span class="sxs-lookup"><span data-stu-id="2d38e-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="2d38e-106">Оболочка Windows предоставляет мощный набор объектов автоматизации, позволяющих программировать оболочку с помощью Microsoft Visual Basic и языков сценариев, таких как Microsoft JScript (совместимы с ECMA 262 языка) и Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2d38e-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="2d38e-107">Эти объекты можно использовать для доступа ко многим функциям и диалоговым окнам оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d38e-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="2d38e-108">Например, можно получить доступ к файловой системе, запустить программы и изменить параметры системы.</span><span class="sxs-lookup"><span data-stu-id="2d38e-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="2d38e-109">В этом разделе представлены объекты оболочки, поддерживающие скрипты.</span><span class="sxs-lookup"><span data-stu-id="2d38e-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="2d38e-110">Версии оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="2d38e-111">Создание экземпляров объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="2d38e-112">Позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="2d38e-113">HTML-элемент OBJECT</span><span class="sxs-lookup"><span data-stu-id="2d38e-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="2d38e-114">Объект оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="2d38e-115">Безопасность</span><span class="sxs-lookup"><span data-stu-id="2d38e-115">Security</span></span>](#security)
-   [<span data-ttu-id="2d38e-116">Объекты папки</span><span class="sxs-lookup"><span data-stu-id="2d38e-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="2d38e-117">Версии оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-117">Shell Versions</span></span>

<span data-ttu-id="2d38e-118">Многие объекты оболочки стали доступны в [версии 4,71](versions.md) оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d38e-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="2d38e-119">Другие доступны в версии 5,00 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2d38e-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="2d38e-120">Версия 5,00 стала доступна в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2d38e-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="2d38e-121">В следующей таблице перечислены все объекты оболочки в версии оболочки, в которой объект стал доступным.</span><span class="sxs-lookup"><span data-stu-id="2d38e-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="2d38e-122">Версия 4,71</span><span class="sxs-lookup"><span data-stu-id="2d38e-122">Version 4.71</span></span>                                            | <span data-ttu-id="2d38e-123">Версия 5,00</span><span class="sxs-lookup"><span data-stu-id="2d38e-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="2d38e-124">**Folder**</span><span class="sxs-lookup"><span data-stu-id="2d38e-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="2d38e-125">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="2d38e-126">**фолдеритемверб**</span><span class="sxs-lookup"><span data-stu-id="2d38e-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="2d38e-127">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="2d38e-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="2d38e-128">**фолдеритемвербс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="2d38e-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="2d38e-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2d38e-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="2d38e-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="2d38e-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="2d38e-132">**шеллфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="2d38e-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="2d38e-133">**фолдеритемс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="2d38e-134">**шеллуихелпер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="2d38e-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="2d38e-136">**шеллвиндовс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="2d38e-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="2d38e-138">**вебвиевфолдерконтентс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="2d38e-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="2d38e-140">**шеллфолдеритем**</span><span class="sxs-lookup"><span data-stu-id="2d38e-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="2d38e-141">**шеллфолдервиевок**</span><span class="sxs-lookup"><span data-stu-id="2d38e-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="2d38e-142">**шелллинкобжект**</span><span class="sxs-lookup"><span data-stu-id="2d38e-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="2d38e-143">Создание экземпляров объектов оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="2d38e-144">Чтобы создать экземпляр объектов оболочки в Visual Basic приложениях с ранней привязкой, добавьте ссылки на следующие библиотеки в проекте:</span><span class="sxs-lookup"><span data-stu-id="2d38e-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="2d38e-145">Элементы управления Microsoft Internet (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="2d38e-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="2d38e-146">Элементы управления и автоматизации Microsoft Shell (shell32)</span><span class="sxs-lookup"><span data-stu-id="2d38e-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="2d38e-147">Позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-147">Late Binding</span></span>

<span data-ttu-id="2d38e-148">Кроме того, можно создать экземпляры многих объектов оболочки с помощью позднего связывания.</span><span class="sxs-lookup"><span data-stu-id="2d38e-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="2d38e-149">Этот подход работает в Visual Basic приложениях и в сценарии.</span><span class="sxs-lookup"><span data-stu-id="2d38e-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="2d38e-150">В следующем примере показано, как создать экземпляр объекта [**оболочки**](shell.md) в JScript.</span><span class="sxs-lookup"><span data-stu-id="2d38e-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="2d38e-151">В следующем примере показано, как создать экземпляр объекта [**Folder**](folder.md) в VBScript.</span><span class="sxs-lookup"><span data-stu-id="2d38e-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="2d38e-152">В предыдущем примере *сдир* — это путь к объекту [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="2d38e-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="2d38e-153">Обратите внимание, что значения перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) недоступны в скрипте.</span><span class="sxs-lookup"><span data-stu-id="2d38e-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="2d38e-154">Идентификатор ProgID для каждого из объектов оболочки показан в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2d38e-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="2d38e-155">Объект</span><span class="sxs-lookup"><span data-stu-id="2d38e-155">Object</span></span>                                                  | <span data-ttu-id="2d38e-156">ProgID:</span><span class="sxs-lookup"><span data-stu-id="2d38e-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d38e-157">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="2d38e-158">Microsoft. Дисккуота. 1</span><span class="sxs-lookup"><span data-stu-id="2d38e-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="2d38e-159">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="2d38e-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="2d38e-160">Не удается выполнить позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="2d38e-161">**Folder**</span><span class="sxs-lookup"><span data-stu-id="2d38e-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="2d38e-162">консоль. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="2d38e-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="2d38e-163">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="2d38e-164">консоль. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="2d38e-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="2d38e-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="2d38e-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="2d38e-166">консоль. Shell \_ Application. Namespace ("..."). Self или Folder. Items. Item или Folder. ParseName</span><span class="sxs-lookup"><span data-stu-id="2d38e-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="2d38e-167">**фолдеритемс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="2d38e-168">Папка. элементы</span><span class="sxs-lookup"><span data-stu-id="2d38e-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="2d38e-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="2d38e-170">Папка. элементы</span><span class="sxs-lookup"><span data-stu-id="2d38e-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="2d38e-171">**фолдеритемверб**</span><span class="sxs-lookup"><span data-stu-id="2d38e-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="2d38e-172">Shell. NameSpace ("..."). Собственные глаголы. Item ()</span><span class="sxs-lookup"><span data-stu-id="2d38e-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="2d38e-173">**фолдеритемвербс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="2d38e-174">FolderItem. Verbs или Shell. NameSpace ("..."). Собственные глаголы</span><span class="sxs-lookup"><span data-stu-id="2d38e-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="2d38e-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="2d38e-176">консоль. \_Приложение оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="2d38e-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="2d38e-178">Shell. NameSpace ("..."). Self. Link или Shell. NameSpace ("..."). Items (). Соединение</span><span class="sxs-lookup"><span data-stu-id="2d38e-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="2d38e-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2d38e-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="2d38e-180">консоль. \_Приложение оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="2d38e-181">**шеллфолдеритем**</span><span class="sxs-lookup"><span data-stu-id="2d38e-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="2d38e-182">Shell. NameSpace ("..."). Self или Shell. NameSpace ("..."). Items ()</span><span class="sxs-lookup"><span data-stu-id="2d38e-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="2d38e-183">**шеллфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="2d38e-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="2d38e-184">Не удается выполнить позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="2d38e-185">**шеллфолдервиевок**</span><span class="sxs-lookup"><span data-stu-id="2d38e-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="2d38e-186">Не удается выполнить позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="2d38e-187">**шелллинкобжект**</span><span class="sxs-lookup"><span data-stu-id="2d38e-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="2d38e-188">Shell. NameSpace ("..."). Self. Link или Shell. NameSpace ("..."). Items (). Соединение</span><span class="sxs-lookup"><span data-stu-id="2d38e-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="2d38e-189">**шеллуихелпер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="2d38e-190">Не удается выполнить позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="2d38e-191">**шеллвиндовс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="2d38e-192">консоль. \_Окна оболочки или шеллвиндовс. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="2d38e-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="2d38e-193">**вебвиевфолдерконтентс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="2d38e-194">Не удается выполнить позднее связывание</span><span class="sxs-lookup"><span data-stu-id="2d38e-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="2d38e-195">HTML-элемент OBJECT</span><span class="sxs-lookup"><span data-stu-id="2d38e-195">HTML OBJECT Element</span></span>

<span data-ttu-id="2d38e-196">Элемент [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) можно также использовать для создания экземпляров объектов оболочки на HTML-странице.</span><span class="sxs-lookup"><span data-stu-id="2d38e-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="2d38e-197">Для этого задайте для атрибута **ID** элемента **Object** имя переменной, которая будет использоваться в скриптах, и укажите объект, используя его зарегистрированный номер (ClassID).</span><span class="sxs-lookup"><span data-stu-id="2d38e-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="2d38e-198">Следующий HTML-код создает экземпляр объекта [**шеллфолдеритем**](shellfolderitem-object.md) с помощью элемента **Object** .</span><span class="sxs-lookup"><span data-stu-id="2d38e-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="2d38e-199">В следующей таблице перечислены все объекты оболочки и соответствующие ИДЕНТИФИКАТОРы классов.</span><span class="sxs-lookup"><span data-stu-id="2d38e-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="2d38e-200">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="2d38e-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="2d38e-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="2d38e-202">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="2d38e-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="2d38e-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="2d38e-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="2d38e-204">**Folder**</span><span class="sxs-lookup"><span data-stu-id="2d38e-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="2d38e-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="2d38e-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="2d38e-206">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="2d38e-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="2d38e-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="2d38e-208">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="2d38e-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="2d38e-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="2d38e-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="2d38e-210">**фолдеритемс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="2d38e-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="2d38e-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="2d38e-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="2d38e-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="2d38e-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="2d38e-214">**фолдеритемверб**</span><span class="sxs-lookup"><span data-stu-id="2d38e-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="2d38e-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="2d38e-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="2d38e-216">**фолдеритемвербс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="2d38e-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="2d38e-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="2d38e-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="2d38e-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="2d38e-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="2d38e-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="2d38e-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="2d38e-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="2d38e-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="2d38e-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2d38e-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="2d38e-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="2d38e-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="2d38e-224">**шеллфолдеритем**</span><span class="sxs-lookup"><span data-stu-id="2d38e-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="2d38e-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="2d38e-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="2d38e-226">**шеллфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="2d38e-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="2d38e-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="2d38e-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="2d38e-228">**шеллфолдервиевок**</span><span class="sxs-lookup"><span data-stu-id="2d38e-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="2d38e-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="2d38e-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="2d38e-230">**шелллинкобжект**</span><span class="sxs-lookup"><span data-stu-id="2d38e-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="2d38e-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="2d38e-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="2d38e-232">**шеллуихелпер**</span><span class="sxs-lookup"><span data-stu-id="2d38e-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="2d38e-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="2d38e-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="2d38e-234">**шеллвиндовс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="2d38e-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="2d38e-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="2d38e-236">**вебвиевфолдерконтентс**</span><span class="sxs-lookup"><span data-stu-id="2d38e-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="2d38e-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="2d38e-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="2d38e-238">Объект оболочки</span><span class="sxs-lookup"><span data-stu-id="2d38e-238">Shell Object</span></span>

<span data-ttu-id="2d38e-239">Объект [**оболочки**](shell.md) представляет объекты в оболочке.</span><span class="sxs-lookup"><span data-stu-id="2d38e-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="2d38e-240">Методы, предоставляемые объектом Shell, можно использовать для:</span><span class="sxs-lookup"><span data-stu-id="2d38e-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="2d38e-241">Открывать, изучать и просматривать папки;</span><span class="sxs-lookup"><span data-stu-id="2d38e-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="2d38e-242">Сократите, восстановите, каскадное или мозаичное открытие окон.</span><span class="sxs-lookup"><span data-stu-id="2d38e-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="2d38e-243">Запуск приложений панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d38e-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="2d38e-244">Отображает системные диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="2d38e-244">Display system dialog boxes.</span></span>

<span data-ttu-id="2d38e-245">Пользователи, возможно, знакомы с командами, к которым они обращаются из меню « **Пуск** » и с контекстным меню панели задач.</span><span class="sxs-lookup"><span data-stu-id="2d38e-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="2d38e-246">Контекстное меню панели задач появляется, когда пользователь правой кнопкой мыши щелкнул панель задач.</span><span class="sxs-lookup"><span data-stu-id="2d38e-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="2d38e-247">Следующее HTML-приложение (HTA) создает начальную страницу с кнопками, которые реализуют многие методы объекта [**оболочки**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="2d38e-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="2d38e-248">Некоторые из этих методов реализуют функции в меню « **Пуск** » и в контекстном меню панели задач.</span><span class="sxs-lookup"><span data-stu-id="2d38e-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="2d38e-249">Безопасность</span><span class="sxs-lookup"><span data-stu-id="2d38e-249">Security</span></span>

<span data-ttu-id="2d38e-250">Как приложение, HTA выполняется с использованием другой модели безопасности, чем веб-страница.</span><span class="sxs-lookup"><span data-stu-id="2d38e-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="2d38e-251">Для взаимодействия с веб-страницей, реализующей функциональные возможности объектов оболочки, пользователи должны включить **элементы управления ActiveX "инициализировать" и "Скрипт", не помеченные как "безопасный** " для зоны безопасности, в которой они просматривают страницу.</span><span class="sxs-lookup"><span data-stu-id="2d38e-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="2d38e-252">Объекты папки</span><span class="sxs-lookup"><span data-stu-id="2d38e-252">Folder Objects</span></span>

<span data-ttu-id="2d38e-253">Объект [**Folder**](folder.md) представляет папку оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d38e-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="2d38e-254">Методы, предоставляемые объектом Folder, можно использовать для:</span><span class="sxs-lookup"><span data-stu-id="2d38e-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="2d38e-255">Получение сведений о папке.</span><span class="sxs-lookup"><span data-stu-id="2d38e-255">Get information about a folder.</span></span>
-   <span data-ttu-id="2d38e-256">Создание вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="2d38e-256">Create subfolders.</span></span>
-   <span data-ttu-id="2d38e-257">Копирование и перемещение объектов File в папку.</span><span class="sxs-lookup"><span data-stu-id="2d38e-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="2d38e-258">Объект [**FolderItem**](folderitem.md) представляет элемент в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d38e-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="2d38e-259">Его свойства позволяют получать сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="2d38e-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="2d38e-260">Методы, предоставляемые этим объектом, можно использовать для выполнения глаголов элемента или для получения сведений об объекте [**фолдеритемвербс**](folderitemverbs.md) элемента.</span><span class="sxs-lookup"><span data-stu-id="2d38e-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="2d38e-261">Объект [**фолдеритемс**](folderitems.md) представляет коллекцию элементов в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="2d38e-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="2d38e-262">Его методы и свойства позволяют получать сведения о коллекции.</span><span class="sxs-lookup"><span data-stu-id="2d38e-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="2d38e-263">В следующем Visual Basic примере показана связь между несколькими объектами папки и их совместное использование.</span><span class="sxs-lookup"><span data-stu-id="2d38e-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="2d38e-264">Когда пользователь нажимает кнопку Command с именем **кмджетпас**, программа отображает диалоговое окно, позволяющее пользователю выбрать папку из **Мой компьютер**, где Ссфдривес — значение перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) для **Мой компьютер**.</span><span class="sxs-lookup"><span data-stu-id="2d38e-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="2d38e-265">Когда пользователь выбирает папку, путь к папке отображается в текстовом поле с именем **ткстпас**.</span><span class="sxs-lookup"><span data-stu-id="2d38e-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="2d38e-266">В VBScript эта функция немного отличается, так как значения перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) недоступны в скрипте.</span><span class="sxs-lookup"><span data-stu-id="2d38e-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="2d38e-267">В следующем примере показан пример VBScript, эквивалентный предыдущему примеру.</span><span class="sxs-lookup"><span data-stu-id="2d38e-267">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="2d38e-268">В следующем примере JScript, который является прямым переводом предыдущего примера VBScript, обратите внимание на то, как пустые скобки "()" используются для вызова [**элементов**](folder-items.md) и методов [**элементов**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2d38e-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 

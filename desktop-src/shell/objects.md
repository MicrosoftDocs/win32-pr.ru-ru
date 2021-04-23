---
description: В этом разделе описываются объекты Windows, реализованные оболочкой.
title: Объекты оболочки для сценариев и Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545922"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="7eb8d-103">Объекты оболочки для сценариев и Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7eb8d-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="7eb8d-104">В этом разделе описываются объекты Windows, реализованные оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7eb8d-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7eb8d-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eb8d-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="7eb8d-106">Topic</span></span></th>
<th><span data-ttu-id="7eb8d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7eb8d-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7eb8d-108"><a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-109">Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="7eb8d-110">Этот объект делает необходимые функции интерфейса <a href="didiskquotauser-object.md"><strong>дидисккуотаусер</strong></a> доступными для создания сценариев и приложений на основе Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-111"><a href="diskquotacontrol-object.md"><strong>дисккуотаконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-112">Позволяет администратору управлять свойствами дисковой квоты тома.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="7eb8d-113">Файловая система NTFS позволяет администратору управлять использованием дискового пространства на общем томе, выделяя заданный объем места на диске или <em>предельную квоту</em>для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="7eb8d-114">Этот объект можно использовать для задания предельной квоты по умолчанию, которая будет автоматически назначена всем новым пользователям.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-115"><a href="dshellwindowsevents.md"><strong>дшеллвиндовсевентс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-116">Получает события регистрации окна <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>ишеллвиндовс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-117"><a href="folder.md"><strong>Folder</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-118">Представляет папку оболочки.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-118">Represents a Shell folder.</span></span> <span data-ttu-id="7eb8d-119">Этот объект содержит свойства и методы, позволяющие получить сведения о папке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-121">Расширяет объект <a href="folder.md"><strong>Folder</strong></a> для поддержки автономных папок.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-123">Представляет элемент в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="7eb8d-124">Этот объект содержит свойства и методы, позволяющие получить сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-125"><a href="folderitems.md"><strong>фолдеритемс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-126">Представляет коллекцию элементов в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="7eb8d-127">Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-129">Расширяет объект <a href="folderitems.md"><strong>фолдеритемс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="7eb8d-130">Он поддерживает один дополнительный метод.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-132">Расширяет объект <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="7eb8d-133">Этот объект поддерживает дополнительный метод и свойство.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-134"><a href="folderitemverb.md"><strong>фолдеритемверб</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-135">Представляет единственную команду, доступную для элемента.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="7eb8d-136">Этот объект содержит свойства и методы, позволяющие получить сведения о команде.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-137"><a href="folderitemverbs.md"><strong>фолдеритемвербс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-138">Представляет коллекцию команд для элемента в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="7eb8d-139">Этот объект содержит свойства и методы, позволяющие получить сведения о коллекции.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-140"><a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-141">Представляет объект в оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-141">Represents an object in the Shell.</span></span> <span data-ttu-id="7eb8d-142">Предоставляются методы для управления оболочкой и выполнения команд в оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="7eb8d-143">Существуют также методы для получения других объектов, связанных с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-144">
<a href="ishelldispatch.md"><strong>Ишеллдиспатч</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-146">Расширяет объект <a href="ishelldispatch.md"><strong>ишеллдиспатч</strong></a> с помощью ряда новых функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-149">Расширяет объект <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="7eb8d-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> поддерживает один новый метод в дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch2</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-153">Расширяет объект <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="7eb8d-154">В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> поддерживает четыре дополнительных метода.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-157">Расширяет объект <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="7eb8d-158">В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> добавляет метод, который отображает открытые окна в трехмерном стеке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-161">Расширяет объект <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="7eb8d-162">В дополнение к свойствам и методам, поддерживаемым <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> добавляет метод, отображающий панель поиска приложений.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="7eb8d-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> реализован и доступен через объект <a href="shell.md"><strong>Shell</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-165">Расширяет объект <a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a> и поддерживает одно дополнительное свойство.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-166"><a href="newwdevents.md"><strong>неввдевентс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-167">Расширяет объект <a href="webwizardhost.md"><strong>вебвизардхост</strong></a> , позволяя страницам на стороне сервера, размещенным в мастере, проверять, что пользователь прошел проверку подлинности с помощью учетная запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-169">Представляет объекты в оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="7eb8d-170">Предоставляются методы для управления оболочкой и выполнения команд в оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="7eb8d-171">Существуют также методы для получения других объектов, связанных с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-172"><a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-173">Расширяет объект <a href="folderitem.md"><strong>FolderItem</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="7eb8d-174">В дополнение к свойствам и методам, поддерживаемым <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>шеллфолдеритем</strong></a> имеет два дополнительных метода.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-175"><a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-176">Представляет объекты в представлении и предоставляет свойства и методы, используемые для получения сведений о содержимом представления.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-177"><a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-178">Перенаправляет события, инициируемые указанным объектом <a href="shellfolderview.md"><strong>шеллфолдервиев</strong></a> , в соответствующие обработчики событий <a href="shellfolderviewoc-object.md"><strong>шеллфолдервиевок</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb8d-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-179"><a href="shelllinkobject-object.md"><strong>шелллинкобжект</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-180">Управляет связями оболочки.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-180">Manages Shell links.</span></span> <span data-ttu-id="7eb8d-181">Этот объект делает большую часть функциональных возможностей интерфейса <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>ишелллинк</strong></a> , доступного для сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-182"><a href="shelluihelper.md"><strong>шеллуихелпер</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-183">Реализовано оболочкой, чтобы помочь скриптам и Visual Basic разработчикам использовать некоторые функции, доступные в оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="7eb8d-184">Объект <a href="shelluihelper.md"><strong>шеллуихелпер</strong></a> не имеет свойств или событий.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="7eb8d-185">Для добавления элементов в оболочку предоставляются методы.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb8d-186"><a href="shellwindows.md"><strong>шеллвиндовс</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-187">Представляет коллекцию открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="7eb8d-188">Методы, связанные с этими объектами, могут управлять и выполнять команды в оболочке и получать другие объекты, связанные с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb8d-189"><a href="webwizardhost.md"><strong>вебвизардхост</strong></a></span><span class="sxs-lookup"><span data-stu-id="7eb8d-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="7eb8d-190">Предоставляет методы, позволяющие HTML-страницам, размещенным в расширении мастера, взаимодействовать с мастером.</span><span class="sxs-lookup"><span data-stu-id="7eb8d-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





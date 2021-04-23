---
description: 'Система хранит сведения о профиле пользователя в определенном каталоге с разными именами в разных версиях Windows: &\# 0034; Documents and Settings&\# 0034; в Windows XP и &\# 0034; Пользователи&\# 0034; в Windows Vista и более поздних версиях.'
title: Каталог профилей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985636"
---
# <a name="profiles-directory"></a><span data-ttu-id="1d947-103">Каталог профилей</span><span class="sxs-lookup"><span data-stu-id="1d947-103">Profiles Directory</span></span>

<span data-ttu-id="1d947-104">Система хранит сведения о профиле пользователя в определенном каталоге с разными именами в разных версиях Windows: «Documents and Settings» в Windows XP и «Users» в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1d947-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="1d947-105">Чтобы получить путь к каталогу Profiles, используйте функцию [**жетпрофилесдиректори**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="1d947-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="1d947-106">Каталог Profiles содержит следующие подкаталоги для профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="1d947-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="1d947-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="1d947-107">Directory</span></span>                                      | <span data-ttu-id="1d947-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1d947-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d947-109">Папка ProgramData (Windows Vista или более поздней версии), пользователи/ALL</span><span class="sxs-lookup"><span data-stu-id="1d947-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="1d947-110">Сведения о программе, применимые ко всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="1d947-110">Program information that applies to all users.</span></span> <span data-ttu-id="1d947-111">Каталог все пользователи по-прежнему существует в Windows Vista или более поздней версии для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="1d947-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="1d947-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1d947-112">Default</span></span>                                        | <span data-ttu-id="1d947-113">Сведения о профиле, которые применяются к пользователю по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d947-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="1d947-114">*Пользователь*</span><span class="sxs-lookup"><span data-stu-id="1d947-114">*User*</span></span>                                         | <span data-ttu-id="1d947-115">Сведения о профиле, применимые к указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="1d947-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="1d947-116">Каждый пользователь имеет свой подкаталог профиля.</span><span class="sxs-lookup"><span data-stu-id="1d947-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="1d947-117">Чтобы получить расположение каталога папка ProgramData/All Users, вызовите функцию [**жеталлусерспрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="1d947-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="1d947-118">Этот каталог содержит следующие подкаталоги:</span><span class="sxs-lookup"><span data-stu-id="1d947-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="1d947-119">Каталог</span><span class="sxs-lookup"><span data-stu-id="1d947-119">Directory</span></span>  | <span data-ttu-id="1d947-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1d947-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="1d947-121">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="1d947-121">Desktop</span></span>    | <span data-ttu-id="1d947-122">Ярлыки, отображаемые на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="1d947-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="1d947-123">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="1d947-123">Start Menu</span></span> | <span data-ttu-id="1d947-124">Пункты меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="1d947-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="1d947-125">Чтобы получить расположение каталога пользователя по умолчанию, вызовите функцию [**жетдефаултусерпрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="1d947-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="1d947-126">Чтобы получить расположение каталога конкретного пользователя, вызовите функцию [**жетусерпрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="1d947-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="1d947-127">Как пользователь по умолчанию, так и конкретные каталоги пользователей содержат следующие подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="1d947-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="1d947-128">Каталоги в курсиве обозначают каталоги, которые по умолчанию скрыты.</span><span class="sxs-lookup"><span data-stu-id="1d947-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="1d947-129">Эти каталоги можно просмотреть, выбрав параметр **Показать скрытые файлы, папки и диски** в элементе панели управления " **Свойства папки** ".</span><span class="sxs-lookup"><span data-stu-id="1d947-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d947-130">Каталог</span><span class="sxs-lookup"><span data-stu-id="1d947-130">Directory</span></span></th>
<th><span data-ttu-id="1d947-131">Описание</span><span class="sxs-lookup"><span data-stu-id="1d947-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d947-132">Данные приложений</span><span class="sxs-lookup"><span data-stu-id="1d947-132">Application Data</span></span></td>
<td><span data-ttu-id="1d947-133">Данные конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="1d947-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-134">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="1d947-134">Cookies</span></span></td>
<td><span data-ttu-id="1d947-135">Файлы cookie Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1d947-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d947-136">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="1d947-136">Desktop</span></span></td>
<td><span data-ttu-id="1d947-137">Ярлыки, отображаемые на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="1d947-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-138">Избранное</span><span class="sxs-lookup"><span data-stu-id="1d947-138">Favorites</span></span></td>
<td><span data-ttu-id="1d947-139">Ссылки на избранные веб-сайты.</span><span class="sxs-lookup"><span data-stu-id="1d947-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d947-140">Локальные параметры</span><span class="sxs-lookup"><span data-stu-id="1d947-140">Local Settings</span></span></td>
<td><span data-ttu-id="1d947-141">Параметры приложения и данные, которые не перемещаются вместе с профилем.</span><span class="sxs-lookup"><span data-stu-id="1d947-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="1d947-142">Обычно параметры или данные в этом каталоге относятся к конкретному компьютеру или слишком велики для эффективного перемещения.</span><span class="sxs-lookup"><span data-stu-id="1d947-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="1d947-143">Этот каталог содержит следующие вложенные папки:</span><span class="sxs-lookup"><span data-stu-id="1d947-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="1d947-144">Данные приложений</span><span class="sxs-lookup"><span data-stu-id="1d947-144">Application Data</span></span></li>
<li><span data-ttu-id="1d947-145">Журнал</span><span class="sxs-lookup"><span data-stu-id="1d947-145">History</span></span></li>
<li><span data-ttu-id="1d947-146">Temp</span><span class="sxs-lookup"><span data-stu-id="1d947-146">Temp</span></span></li>
<li><span data-ttu-id="1d947-147">"Временные файлы Интернета".</span><span class="sxs-lookup"><span data-stu-id="1d947-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-148">Мои документы</span><span class="sxs-lookup"><span data-stu-id="1d947-148">My Documents</span></span></td>
<td><span data-ttu-id="1d947-149">Расположение по умолчанию для документов, создаваемых пользователем.</span><span class="sxs-lookup"><span data-stu-id="1d947-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="1d947-150">По умолчанию приложения должны сохранять файлы документов в этот каталог.</span><span class="sxs-lookup"><span data-stu-id="1d947-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d947-151"><em>несуд</em></span><span class="sxs-lookup"><span data-stu-id="1d947-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="1d947-152">Ярлыки для элементов сетевого окружения.</span><span class="sxs-lookup"><span data-stu-id="1d947-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-153"><em>принсуд</em></span><span class="sxs-lookup"><span data-stu-id="1d947-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="1d947-154">Ярлыки для элементов папки принтера.</span><span class="sxs-lookup"><span data-stu-id="1d947-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d947-155"><em>Последние</em></span><span class="sxs-lookup"><span data-stu-id="1d947-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="1d947-156">Ярлыки для недавно использовавшихся документов.</span><span class="sxs-lookup"><span data-stu-id="1d947-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-157">Cервера</span><span class="sxs-lookup"><span data-stu-id="1d947-157">SendTo</span></span></td>
<td><span data-ttu-id="1d947-158">Ярлыки для мест, в которые пользователь часто отправляет файлы.</span><span class="sxs-lookup"><span data-stu-id="1d947-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1d947-159">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="1d947-159">Start Menu</span></span></td>
<td><span data-ttu-id="1d947-160">Пункты меню " <strong>Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="1d947-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d947-161"><em>Шаблоны</em></span><span class="sxs-lookup"><span data-stu-id="1d947-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="1d947-162">Ярлыки для элементов шаблона.</span><span class="sxs-lookup"><span data-stu-id="1d947-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1d947-163">Чтобы получить расположение подкаталогов этих каталогов, используйте функции [**шжетфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) или [**шжеткновнфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .</span><span class="sxs-lookup"><span data-stu-id="1d947-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 




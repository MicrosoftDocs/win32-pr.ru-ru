---
description: В этом разделе описывается, какие библиотеки и как они могут помочь пользователям и разработчикам.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: О библиотеках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554930"
---
# <a name="about-libraries"></a><span data-ttu-id="0592b-103">О библиотеках</span><span class="sxs-lookup"><span data-stu-id="0592b-103">About Libraries</span></span>

<span data-ttu-id="0592b-104">В этом разделе описывается, какие библиотеки и как они могут помочь пользователям и разработчикам.</span><span class="sxs-lookup"><span data-stu-id="0592b-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="0592b-105">Библиотеки представляют собой определяемые пользователем коллекции папок.</span><span class="sxs-lookup"><span data-stu-id="0592b-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="0592b-106">Библиотека отслеживает физическое место хранения каждой папки, что позволяет отменять пользователя и программное обеспечение этой задачи.</span><span class="sxs-lookup"><span data-stu-id="0592b-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="0592b-107">Пользователи могут группировать связанные папки вместе в библиотеке, даже если эти папки хранятся на разных жестких дисках или на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="0592b-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="0592b-108">В библиотеке папки и файлы отображаются для пользователя как единая коллекция, и с помощью API библиотеки оболочки содержимое библиотеки может также находиться в одном расположении с программой.</span><span class="sxs-lookup"><span data-stu-id="0592b-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="0592b-109">В библиотеке содержимое, например документы пользователя, фотографии, видео или музыку, может быть отсортировано и отображено по мере необходимости, а не просто в соответствии с требованиями файловой системы.</span><span class="sxs-lookup"><span data-stu-id="0592b-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="0592b-110">Например, пользователи могут упорядочивать содержимое библиотеки с помощью свойств элементов в библиотеке, чтобы связанные элементы могли сортироваться вместе, даже если они хранятся в разных папках.</span><span class="sxs-lookup"><span data-stu-id="0592b-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![снимок экрана с пользовательским интерфейсом библиотек](images/libraries-whatare.png)

<span data-ttu-id="0592b-112">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="0592b-112">In this topic:</span></span>

-   [<span data-ttu-id="0592b-113">Преимущества библиотеки</span><span class="sxs-lookup"><span data-stu-id="0592b-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="0592b-114">Преимущества для пользователей</span><span class="sxs-lookup"><span data-stu-id="0592b-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="0592b-115">Преимущества для разработчиков</span><span class="sxs-lookup"><span data-stu-id="0592b-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="0592b-116">Управление папками в библиотеках</span><span class="sxs-lookup"><span data-stu-id="0592b-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="0592b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0592b-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="0592b-118">Преимущества библиотеки</span><span class="sxs-lookup"><span data-stu-id="0592b-118">Library Benefits</span></span>

<span data-ttu-id="0592b-119">В этом разделе описываются некоторые преимущества библиотек с точки зрения конечного пользователя и точки зрения разработчика программы.</span><span class="sxs-lookup"><span data-stu-id="0592b-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="0592b-120">Преимущества для пользователей</span><span class="sxs-lookup"><span data-stu-id="0592b-120">User Benefits</span></span>

<span data-ttu-id="0592b-121">Добавление в программу поддержки библиотек предоставляет пользователю следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="0592b-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="0592b-122">**Библиотеки предоставляют единообразный пользовательский интерфейс в Windows 7**</span><span class="sxs-lookup"><span data-stu-id="0592b-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="0592b-123">Общие диалоговые окна файлов поддерживают библиотеки и предоставляют те же возможности, что и проводник Windows в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0592b-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="0592b-124">Поддержка библиотек в программе поможет обеспечить более эффективное взаимодействие с пользователем при использовании программы в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0592b-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="0592b-125">**Пользователи решают, где хранить содержимое**</span><span class="sxs-lookup"><span data-stu-id="0592b-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="0592b-126">Библиотеки позволяют пользователям управлять местом хранения содержимого.</span><span class="sxs-lookup"><span data-stu-id="0592b-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="0592b-127">В то же время библиотеки предоставляют пользователям разумные значения по умолчанию, которые не хотят управлять этим уровнем детализации на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="0592b-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="0592b-128">Пользователи определяют, сколько и сколько элементов управления нужно контролировать, где и как хранится их содержимое, и библиотека работает правильно.</span><span class="sxs-lookup"><span data-stu-id="0592b-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="0592b-129">Преимущества для разработчиков</span><span class="sxs-lookup"><span data-stu-id="0592b-129">Developer Benefits</span></span>

<span data-ttu-id="0592b-130">Библиотеки в программе можно использовать для предоставления более гибкого и удобного пользовательского интерфейса без необходимости добавлять множество сложных программных программ.</span><span class="sxs-lookup"><span data-stu-id="0592b-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="0592b-131">Ниже перечислены некоторые преимущества добавления поддержки библиотек.</span><span class="sxs-lookup"><span data-stu-id="0592b-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="0592b-132">**Библиотеки поддерживают доступ к библиотеке и файловой системе**</span><span class="sxs-lookup"><span data-stu-id="0592b-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="0592b-133">С помощью [**API библиотеки оболочки**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)программы могут предоставлять пользователю поддержку библиотек, уменьшая сложность кода управления файлами и папками.</span><span class="sxs-lookup"><span data-stu-id="0592b-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="0592b-134">Если программа уже использует API файловой системы, можно сохранить как можно большую часть существующего кода и по-прежнему предоставлять пользователю поддержку библиотеки, получая необходимые сведения о файловой системе из **API библиотеки оболочки**.</span><span class="sxs-lookup"><span data-stu-id="0592b-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="0592b-135">**Упрощенное уведомление об изменении**</span><span class="sxs-lookup"><span data-stu-id="0592b-135">**Simpler change notification**</span></span>

    <span data-ttu-id="0592b-136">Как файловая система, так и API оболочки могут уведомлять программу при изменении содержимого наблюдаемой папки или библиотеки.</span><span class="sxs-lookup"><span data-stu-id="0592b-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="0592b-137">Однако с помощью API оболочки можно отслеживать все папки в библиотеке с помощью одного уведомления, даже несмотря на то, что папка в библиотеке может храниться на разных дисках или даже на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="0592b-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="0592b-138">**Библиотеки используют свойства файлов**</span><span class="sxs-lookup"><span data-stu-id="0592b-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="0592b-139">Программы могут использовать свойства файла для управления отображением файлов во время операций открытия и сохранения, использующих общие диалоговые окна файла.</span><span class="sxs-lookup"><span data-stu-id="0592b-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="0592b-140">Программы также могут иметь доступ к свойствам файла с помощью интерфейсов [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="0592b-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="0592b-141">Общие диалоговые окна файла также можно настроить, чтобы пользователи могли обновлять свойства, связанные с их содержимым.</span><span class="sxs-lookup"><span data-stu-id="0592b-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="0592b-142">**Программы могут создавать выделенные библиотеки**</span><span class="sxs-lookup"><span data-stu-id="0592b-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="0592b-143">Новая библиотека может быть создана, если существующие пользовательские библиотеки не соответствуют потребностям программы, например, если программа создает новый тип содержимого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0592b-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="0592b-144">Новую библиотеку можно настроить с помощью уникального значка, который представляет их содержимое, и упрощает обнаружение библиотеки в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="0592b-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="0592b-145">Управление папками в библиотеках</span><span class="sxs-lookup"><span data-stu-id="0592b-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="0592b-146">Пользователи могут упорядочивать свои библиотеки, добавляя, перемещая или удаляя папки в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0592b-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="0592b-147">Однако не все папки поддерживают все функции, которые может предоставить библиотека.</span><span class="sxs-lookup"><span data-stu-id="0592b-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="0592b-148">Многие функции библиотеки нуждаются в быстром доступе к различным свойствам папки и ее содержимому, доступным только в Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0592b-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="0592b-149">Чтобы обеспечить полную функциональность библиотеки, папка должна быть доступна для индексирования с помощью службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="0592b-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="0592b-150">Библиотека не позволяет пользователю добавлять папки, которые не предоставляют полную функциональность библиотеки.</span><span class="sxs-lookup"><span data-stu-id="0592b-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="0592b-151">Однако [**API библиотеки оболочки**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) могут добавлять такие папки.</span><span class="sxs-lookup"><span data-stu-id="0592b-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="0592b-152">Если библиотека содержит папку, которая не поддерживает полную функциональность библиотеки, Библиотека будет работает в защищенном режиме и предоставляет ограниченную функциональность.</span><span class="sxs-lookup"><span data-stu-id="0592b-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="0592b-153">В следующей таблице описаны папки, поддерживающие полную функциональность библиотеки, и те, которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0592b-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="0592b-154">Типы папок, поддерживающие полную функциональность библиотеки</span><span class="sxs-lookup"><span data-stu-id="0592b-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="0592b-155">Типы папок, не поддерживающие полную функциональность библиотеки</span><span class="sxs-lookup"><span data-stu-id="0592b-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0592b-156">Фиксированные и внешние жесткие диски NTFS и FAT32.</span><span class="sxs-lookup"><span data-stu-id="0592b-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="0592b-157">Съемные диски, такие как флэш-накопители USB или карты памяти Secure Digital (SD).</span><span class="sxs-lookup"><span data-stu-id="0592b-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="0592b-158">Общие файловые ресурсы, индексируемые службой поиска Windows, например серверы отделов, Windows 7 или домашние компьютеры Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0592b-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="0592b-159">Съемные носители, такие как компакт-диски или DVD-диски.</span><span class="sxs-lookup"><span data-stu-id="0592b-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="0592b-160">Общие файловые ресурсы, доступные автономно, такие как перенаправленная папка " **Мои документы** " или кэш Client-Side.</span><span class="sxs-lookup"><span data-stu-id="0592b-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="0592b-161">Сетевые папки, которые недоступны для автономного или удаленного индексирования, например для дисков NAS.</span><span class="sxs-lookup"><span data-stu-id="0592b-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="0592b-162">Другие источники данных, такие как Microsoft SharePoint, Microsoft Exchange и Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="0592b-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="0592b-163">На следующем рисунке показано ограниченное отображение содержимого библиотеки в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="0592b-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![открыть диалоговое окно при работе с библиотеками в защищенном режиме](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="0592b-165">См. также</span><span class="sxs-lookup"><span data-stu-id="0592b-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0592b-166">О библиотеках</span><span class="sxs-lookup"><span data-stu-id="0592b-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="0592b-167">**ишелллибрари**</span><span class="sxs-lookup"><span data-stu-id="0592b-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="0592b-168">Ссылки оболочки</span><span class="sxs-lookup"><span data-stu-id="0592b-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="0592b-169">Известные папки</span><span class="sxs-lookup"><span data-stu-id="0592b-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="0592b-170">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="0592b-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 

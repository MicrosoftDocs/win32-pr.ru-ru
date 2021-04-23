---
description: В Windows 7 появились библиотеки, которые предоставляют пользователям единое, согласованное представление файлов, даже если эти файлы хранятся в разных расположениях.
title: Библиотеки Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986128"
---
# <a name="windows-libraries"></a><span data-ttu-id="fc26d-103">Библиотеки Windows</span><span class="sxs-lookup"><span data-stu-id="fc26d-103">Windows Libraries</span></span>

<span data-ttu-id="fc26d-104">В Windows 7 появились библиотеки, которые предоставляют пользователям единое, согласованное представление файлов, даже если эти файлы хранятся в разных расположениях.</span><span class="sxs-lookup"><span data-stu-id="fc26d-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="fc26d-105">Библиотеки могут быть настроены и упорядочены пользователем, а библиотеки могут содержать папки, находящиеся на компьютере пользователя, а также папки, к которым предоставлен общий доступ по сети.</span><span class="sxs-lookup"><span data-stu-id="fc26d-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="fc26d-106">Библиотеки представляют собой более простое представление базовой системы хранения, так как для пользователя файлы и папки в библиотеке отображаются в одном представлении независимо от того, где они физически хранятся.</span><span class="sxs-lookup"><span data-stu-id="fc26d-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="fc26d-107">Разработчикам, создающим новые программы в Windows 7, рекомендуется использовать библиотеки как средства, с помощью которых пользователи взаимодействуют с файлами, используемыми программой.</span><span class="sxs-lookup"><span data-stu-id="fc26d-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="fc26d-108">Использование библиотек в программе предоставляет пользователям более четкое, простое и более стабильное взаимодействие в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc26d-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="fc26d-109">Разработчики также должны проанализировать существующие программы и при необходимости обновить их для работы с библиотеками.</span><span class="sxs-lookup"><span data-stu-id="fc26d-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="fc26d-110">Поскольку библиотеки не являются частью файловой системы, API-интерфейсы на основе файловой системы не будут иметь доступа к библиотекам, которые могли быть настроены пользователем.</span><span class="sxs-lookup"><span data-stu-id="fc26d-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="fc26d-111">Программы, которые в настоящее время разрешают пользователям хранить свое содержимое в разных папках или на разных компьютерах, будут использовать наиболее выгодные преимущества при добавлении поддержки библиотек.</span><span class="sxs-lookup"><span data-stu-id="fc26d-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="fc26d-112">Библиотеки упрощают управление содержимым в различных местах хранения для разработчика и пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc26d-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="fc26d-113">В этом руководство описываются дополнительные сведения о библиотеках, о том, как программы могут работать с библиотеками, а также некоторые способы использования библиотек для улучшения работы пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc26d-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc26d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fc26d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc26d-115">О библиотеках</span><span class="sxs-lookup"><span data-stu-id="fc26d-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="fc26d-116">Использование библиотек в программе</span><span class="sxs-lookup"><span data-stu-id="fc26d-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="fc26d-117">**ишелллибрари**</span><span class="sxs-lookup"><span data-stu-id="fc26d-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="fc26d-118">Ссылки оболочки</span><span class="sxs-lookup"><span data-stu-id="fc26d-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="fc26d-119">Известные папки</span><span class="sxs-lookup"><span data-stu-id="fc26d-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="fc26d-120">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="fc26d-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 

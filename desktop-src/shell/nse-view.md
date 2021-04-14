---
description: Большинство расширений пространства имен являются подмножеством пространства имен оболочки.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Отображение Self-Containedного представления расширения пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985664"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="4c9a2-103">Отображение Self-Containedного представления расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="4c9a2-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="4c9a2-104">Большинство расширений пространства имен являются подмножеством пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="4c9a2-105">При создании точки соединения, как описано в разделе [Указание расположения расширения пространства имен](nse-junction.md), проводник Windows позволяет пользователям переходить к своему расширению пространства имен и из него, как и любые другие папки.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="4c9a2-106">Однако можно также использовать проводник Windows для вывода только содержимого расширения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="4c9a2-107">Этот параметр отображения иногда называется *корневым представлением*.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="4c9a2-108">Обычно корневые представления могут быть предпочтительнее обычно для некоторых типов расширений.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="4c9a2-109">При наличии корневого представления создается новый экземпляр проводника Windows, который отображает содержимое расширения как отдельное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="4c9a2-110">Представление в виде дерева в корневом представлении показывает только те папки, которые являются частью расширения.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="4c9a2-111">Пользователи не могут переходить от корневого представления к другим частям пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="4c9a2-112">Расширения реализуются таким же образом для корневых представлений, как и для обычных представлений.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="4c9a2-113">Единственное различие заключается в способе отображения содержимого расширения проводником Windows.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="4c9a2-114">Также можно иметь обычные и корневые представления одного и того же расширения.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="4c9a2-115">Чтобы открыть представление расширения, необходимо запустить экземпляр Explorer.exe с флагом/root.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="4c9a2-116">Существует несколько различных способов запуска корневого представления в зависимости от природы вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="4c9a2-117">Как использовать точку соединения для открытия корневого представления</span><span class="sxs-lookup"><span data-stu-id="4c9a2-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="4c9a2-118">Использование файла ярлыка для открытия корневого представления</span><span class="sxs-lookup"><span data-stu-id="4c9a2-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="4c9a2-119">Отображение корневого представления файла</span><span class="sxs-lookup"><span data-stu-id="4c9a2-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 




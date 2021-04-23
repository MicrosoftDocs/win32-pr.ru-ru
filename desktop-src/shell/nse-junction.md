---
description: Корень расширения пространства имен обычно отображается в проводнике Windows как папка в представлениях дерева и папок.
title: Указание расположения расширения пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910779"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="94d29-103">Указание расположения расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="94d29-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="94d29-104">Корень расширения пространства имен обычно отображается в проводнике Windows как папка в представлениях дерева и папок.</span><span class="sxs-lookup"><span data-stu-id="94d29-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="94d29-105">Чтобы проводник Windows отображал файлы и вложенные папки расширения, необходимо указать расположение корневой папки в иерархии пространства имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="94d29-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="94d29-106">Это расположение называется *точкой соединения*.</span><span class="sxs-lookup"><span data-stu-id="94d29-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="94d29-107">Использование виртуальных папок в качестве точек соединения</span><span class="sxs-lookup"><span data-stu-id="94d29-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="94d29-108">Использование папок файловой системы в качестве точек соединения</span><span class="sxs-lookup"><span data-stu-id="94d29-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="94d29-109">Открытие представления расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="94d29-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="94d29-110">Использование виртуальных папок в качестве точек соединения</span><span class="sxs-lookup"><span data-stu-id="94d29-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="94d29-111">Самый простой способ определить точку соединения расширения — сделать корневую папку вложенной в системную виртуальную папку.</span><span class="sxs-lookup"><span data-stu-id="94d29-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="94d29-112">Этот тип точки соединения называется *виртуальной точкой соединения*.</span><span class="sxs-lookup"><span data-stu-id="94d29-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="94d29-113">Папки " **Рабочий стол** " и " **Мой компьютер** " представляют собой типичные расположения для точек соединения, но можно также определить виртуальную точку соединения на удаленном компьютере или в папках " **Мое сетевое окружение**", " **Internet Explorer**" и " **Панель управления** ".</span><span class="sxs-lookup"><span data-stu-id="94d29-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="94d29-114">Чтобы определить виртуальную точку соединения, создайте подраздел ключа, который представляет соответствующую виртуальную папку, и присвойте ему строковое представление идентификатора класса (CLSID) расширения.</span><span class="sxs-lookup"><span data-stu-id="94d29-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="94d29-115">Зарегистрированный CLSID будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="94d29-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="94d29-116">*Имя виртуальной папки* является одним из подразделов в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="94d29-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="94d29-117">Расположение</span><span class="sxs-lookup"><span data-stu-id="94d29-117">Location</span></span>          | <span data-ttu-id="94d29-118">Имя виртуальной папки</span><span class="sxs-lookup"><span data-stu-id="94d29-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="94d29-119">Панель управления</span><span class="sxs-lookup"><span data-stu-id="94d29-119">Control Panel</span></span>     | <span data-ttu-id="94d29-120">**контролпанел**</span><span class="sxs-lookup"><span data-stu-id="94d29-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="94d29-121">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="94d29-121">Desktop</span></span>           | <span data-ttu-id="94d29-122">**Рабочий стол**</span><span class="sxs-lookup"><span data-stu-id="94d29-122">**Desktop**</span></span>                                |
| <span data-ttu-id="94d29-123">Вся сеть</span><span class="sxs-lookup"><span data-stu-id="94d29-123">Entire Network</span></span>    | <span data-ttu-id="94d29-124">**Нетворкнеигхборхуд** \\ **Ентиренетворк**</span><span class="sxs-lookup"><span data-stu-id="94d29-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="94d29-125">Мой компьютер</span><span class="sxs-lookup"><span data-stu-id="94d29-125">My Computer</span></span>       | <span data-ttu-id="94d29-126">**Мой**</span><span class="sxs-lookup"><span data-stu-id="94d29-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="94d29-127">Мое сетевое окружение</span><span class="sxs-lookup"><span data-stu-id="94d29-127">My Network Places</span></span> | <span data-ttu-id="94d29-128">**нетворкнеигхборхуд**</span><span class="sxs-lookup"><span data-stu-id="94d29-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="94d29-129">Удаленный компьютер</span><span class="sxs-lookup"><span data-stu-id="94d29-129">Remote Computer</span></span>   | <span data-ttu-id="94d29-130">**ремотекомпутер**</span><span class="sxs-lookup"><span data-stu-id="94d29-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="94d29-131">Файлы пользователей</span><span class="sxs-lookup"><span data-stu-id="94d29-131">Users Files</span></span>       | <span data-ttu-id="94d29-132">**усерсфилес**</span><span class="sxs-lookup"><span data-stu-id="94d29-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="94d29-133">Удаленные расширения должны инициализироваться с помощью [**иремотекомпутер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span><span class="sxs-lookup"><span data-stu-id="94d29-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="94d29-134">Использование папок файловой системы в качестве точек соединения</span><span class="sxs-lookup"><span data-stu-id="94d29-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="94d29-135">Существует два способа определения папок файловой системы в качестве точек соединения.</span><span class="sxs-lookup"><span data-stu-id="94d29-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="94d29-136">Самый простой подход заключается в том, чтобы создать папку в соответствующем расположении и добавить точку в имя папки, а затем в строковом формате идентификатора CLSID расширения.</span><span class="sxs-lookup"><span data-stu-id="94d29-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="94d29-137">В проводнике Windows будет отображаться только имя папки.</span><span class="sxs-lookup"><span data-stu-id="94d29-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="94d29-138">В следующем примере создается точка соединения с отображаемым именем MyFolder.</span><span class="sxs-lookup"><span data-stu-id="94d29-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="94d29-139">В качестве точки соединения можно также определить именованную папку с учетом правил.</span><span class="sxs-lookup"><span data-stu-id="94d29-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="94d29-140">Сделать папку доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94d29-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="94d29-141">Сделайте папку системной папкой, вызвав [**пасмакесистемфолдер**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span><span class="sxs-lookup"><span data-stu-id="94d29-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="94d29-142">Помещение скрытого файла Desktop.ini в папку, содержащую CLSID расширения.</span><span class="sxs-lookup"><span data-stu-id="94d29-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="94d29-143">Desktop.ini — это стандартный текстовый файл, который можно добавить в любую папку для настройки определенных аспектов поведения папки.</span><span class="sxs-lookup"><span data-stu-id="94d29-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="94d29-144">Общие сведения об использовании этого файла см. в статье [Настройка папок с помощью Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="94d29-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="94d29-145">Чтобы определить папку как точку соединения, объект \[ . \] Раздел шеллклассинфо Desktop.ini должен содержать CLSID расширения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="94d29-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="94d29-146">Открытие представления расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="94d29-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="94d29-147">При просмотре пользователем точки соединения проводник Windows автоматически создает представление корневой папки.</span><span class="sxs-lookup"><span data-stu-id="94d29-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="94d29-148">Можно также создать представление, явно запустив Explorer.exe с CLSID расширения в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="94d29-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="94d29-149">Например, этот подход можно использовать для запуска представления расширения из контекстного меню или ярлыка.</span><span class="sxs-lookup"><span data-stu-id="94d29-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="94d29-150">Например, чтобы запустить представление Мекстенсион, включающее представление в виде дерева, можно использовать следующую командную строку.</span><span class="sxs-lookup"><span data-stu-id="94d29-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="94d29-151">Для запуска представления объекта в пределах расширения можно использовать альтернативную командную строку.</span><span class="sxs-lookup"><span data-stu-id="94d29-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="94d29-152">Эта функция может быть полезной, например, для расширения, использующего представление папок, чтобы позволить пользователям просматривать содержимое одного из нескольких сжатых файлов.</span><span class="sxs-lookup"><span data-stu-id="94d29-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="94d29-153">Параметр *objectname* — это имя просматриваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="94d29-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="94d29-154">Проводник Windows преобразует имя в соответствующий ПИДЛ и передает ПИДЛ в метод [**иперсистфолдер:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) нового объекта Folder.</span><span class="sxs-lookup"><span data-stu-id="94d29-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="94d29-155">Строке CLSID должна предшествовать Пара двоеточий (::) или команда завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="94d29-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="94d29-156">Флаг косой черты (/e), используемый в двух приведенных выше примерах командных строк, указывает проводнику Windows отобразить представление в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="94d29-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="94d29-157">Флаг должен быть отделен двумя двоеточиями запятой.</span><span class="sxs-lookup"><span data-stu-id="94d29-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="94d29-158">Если представление в виде дерева не требуется, опустите флаг/e и запятую.</span><span class="sxs-lookup"><span data-stu-id="94d29-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 




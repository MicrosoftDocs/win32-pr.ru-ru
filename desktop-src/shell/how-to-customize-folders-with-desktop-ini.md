---
description: Настройка внешнего вида и поведения отдельной папки с Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Настройка папок с помощью Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581752"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="00c07-103">Настройка папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="00c07-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="00c07-104">Папки файловой системы обычно отображаются со стандартным значком и набором свойств, которые указывают, например, является ли папка общей.</span><span class="sxs-lookup"><span data-stu-id="00c07-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="00c07-105">Внешний вид и поведение отдельной папки можно настроить, создав файл Desktop.ini для этой папки.</span><span class="sxs-lookup"><span data-stu-id="00c07-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="00c07-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="00c07-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="00c07-107">Использование файлов Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="00c07-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="00c07-108">Обычно папки отображаются со стандартным значком папки.</span><span class="sxs-lookup"><span data-stu-id="00c07-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="00c07-109">Обычно файл Desktop.ini используется для назначения в папку пользовательского значка или эскиза.</span><span class="sxs-lookup"><span data-stu-id="00c07-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="00c07-110">Desktop.ini можно использовать для создания *всплывающей подсказки* , которая отображает сведения о папке и управляет некоторыми аспектами поведения папки, например указанием локализованных имен для папки или элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="00c07-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="00c07-111">**Следующая процедура используется для настройки стиля папки с помощью Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="00c07-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="00c07-112">Используйте [**пасмакесистемфолдер**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) , чтобы сделать папку системной.</span><span class="sxs-lookup"><span data-stu-id="00c07-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="00c07-113">Это устанавливает для папки бит только для чтения, чтобы указать, что специальное поведение, зарезервированное для Desktop.ini, должно быть включено.</span><span class="sxs-lookup"><span data-stu-id="00c07-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="00c07-114">Вы также можете создать папку в качестве системной папки из командной строки с помощью команды **attrib + s** *имя_папки*.</span><span class="sxs-lookup"><span data-stu-id="00c07-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="00c07-115">Создайте файл Desktop.ini для папки.</span><span class="sxs-lookup"><span data-stu-id="00c07-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="00c07-116">Его следует пометить как *скрытый* и *системный* , чтобы убедиться, что он скрыт от обычных пользователей.</span><span class="sxs-lookup"><span data-stu-id="00c07-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="00c07-117">Убедитесь, что создаваемый файл Desktop.ini имеет формат Юникода.</span><span class="sxs-lookup"><span data-stu-id="00c07-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="00c07-118">Это необходимо для хранения локализованных строк, которые могут быть отображены пользователям.</span><span class="sxs-lookup"><span data-stu-id="00c07-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="00c07-119">Создание файла Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="00c07-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="00c07-120">Файл Desktop.ini — это текстовый файл, который позволяет указать способ просмотра папки в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="00c07-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="00c07-121">Объект \[ . \] Раздел шеллклассинфо позволяет настроить представление папки, присваивая значения нескольким записям:</span><span class="sxs-lookup"><span data-stu-id="00c07-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

| <span data-ttu-id="00c07-122">Значение</span><span class="sxs-lookup"><span data-stu-id="00c07-122">Value</span></span>             | <span data-ttu-id="00c07-123">Описание</span><span class="sxs-lookup"><span data-stu-id="00c07-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c07-124">**конфирмфилеоп**</span><span class="sxs-lookup"><span data-stu-id="00c07-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="00c07-125">Установите для этой записи значение 0, чтобы избежать предупреждения об удалении системной папки при удалении или перемещении папки.</span><span class="sxs-lookup"><span data-stu-id="00c07-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="00c07-126">**Общий доступ**</span><span class="sxs-lookup"><span data-stu-id="00c07-126">**NoSharing**</span></span>     | <span data-ttu-id="00c07-127">не поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="00c07-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="00c07-128">Установите для этой записи значение 1, чтобы запретить общий доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="00c07-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="00c07-129">**иконфиле**</span><span class="sxs-lookup"><span data-stu-id="00c07-129">**IconFile**</span></span>      | <span data-ttu-id="00c07-130">Если вы хотите указать пользовательский значок для папки, присвойте этой записи имя файла значка.</span><span class="sxs-lookup"><span data-stu-id="00c07-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="00c07-131">Рекомендуется использовать расширение имени файла ICO, но можно также указать .bmp файлы или .exe и .dll файлы, содержащие значки.</span><span class="sxs-lookup"><span data-stu-id="00c07-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="00c07-132">Если используется относительный путь, значок становится доступен пользователям, просматривающим папку по сети.</span><span class="sxs-lookup"><span data-stu-id="00c07-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="00c07-133">Необходимо также задать запись **икониндекс** .</span><span class="sxs-lookup"><span data-stu-id="00c07-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="00c07-134">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="00c07-134">**IconIndex**</span></span>     | <span data-ttu-id="00c07-135">Установите эту запись, чтобы указать индекс для пользовательского значка.</span><span class="sxs-lookup"><span data-stu-id="00c07-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="00c07-136">Если файл, назначенный **иконфиле** , содержит только один значок, задайте для **икониндекс** значение 0.</span><span class="sxs-lookup"><span data-stu-id="00c07-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="00c07-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="00c07-137">**InfoTip**</span></span>       | <span data-ttu-id="00c07-138">Задайте для этой записи информационную текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="00c07-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="00c07-139">Он отображается как всплывающая подсказка при наведении курсора на папку.</span><span class="sxs-lookup"><span data-stu-id="00c07-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="00c07-140">Если пользователь щелкнет папку, текст сведений отображается в информационном блоке папки ниже стандартных сведений.</span><span class="sxs-lookup"><span data-stu-id="00c07-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="00c07-141">Следующие иллюстрации относятся к папке Music с пользовательским файлом Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="00c07-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="00c07-142">Папка теперь:</span><span class="sxs-lookup"><span data-stu-id="00c07-142">The folder now:</span></span>

-   <span data-ttu-id="00c07-143">Имеет пользовательский значок.</span><span class="sxs-lookup"><span data-stu-id="00c07-143">Has a custom icon.</span></span>
-   <span data-ttu-id="00c07-144">Не отображает предупреждение «вы удаляете системную папку», если папка перемещена или удалена.</span><span class="sxs-lookup"><span data-stu-id="00c07-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="00c07-145">Невозможно настроить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="00c07-145">Cannot be shared.</span></span>
-   <span data-ttu-id="00c07-146">Отображает информационный текст при наведении курсора мыши на папку.</span><span class="sxs-lookup"><span data-stu-id="00c07-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="00c07-147">Параметры папки на следующих иллюстрациях настроены для отображения скрытых файлов, чтобы Desktop.ini видна.</span><span class="sxs-lookup"><span data-stu-id="00c07-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="00c07-148">Папка выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00c07-148">The folder looks like this:</span></span>

![снимок экрана папки с настраиваемым значком](images/webview4.jpg)

<span data-ttu-id="00c07-150">При наведении курсора мыши на папку отображается всплывающая подсказка.</span><span class="sxs-lookup"><span data-stu-id="00c07-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![снимок экрана папки с всплывающей подсказкой](images/webview6.jpg)

<span data-ttu-id="00c07-152">Пользовательский значок заменяет значок папки везде, где отображается имя папки.</span><span class="sxs-lookup"><span data-stu-id="00c07-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![снимок экрана пользовательского значка "Замена папки"](images/webview5.jpg)

<span data-ttu-id="00c07-154">Следующий файл desktop.ini использовался для настройки папки Music, как показано на предыдущих иллюстрациях.</span><span class="sxs-lookup"><span data-stu-id="00c07-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 




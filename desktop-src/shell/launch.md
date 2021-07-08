---
description: После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508615"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="9be7d-103">Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)</span><span class="sxs-lookup"><span data-stu-id="9be7d-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="9be7d-104">После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9be7d-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="9be7d-105">Например, приложению может потребоваться запустить другое приложение, позволяющее пользователю изменять файл данных.</span><span class="sxs-lookup"><span data-stu-id="9be7d-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="9be7d-106">Если файл является исполняемым файлом, приложение может захотеть просто запустить его.</span><span class="sxs-lookup"><span data-stu-id="9be7d-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="9be7d-107">В этом документе описывается, как использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="9be7d-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="9be7d-108">Использование ShellExecute и ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="9be7d-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="9be7d-109">Команды объекта</span><span class="sxs-lookup"><span data-stu-id="9be7d-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="9be7d-110">Использование ShellExecuteEx для предоставления служб активации с сайта</span><span class="sxs-lookup"><span data-stu-id="9be7d-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="9be7d-111">Использование ShellExecute для запуска диалогового окна поиска</span><span class="sxs-lookup"><span data-stu-id="9be7d-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="9be7d-112">Простой пример использования ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="9be7d-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="9be7d-113">Использование ShellExecute и ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="9be7d-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="9be7d-114">Чтобы использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), приложение должно указать объект файла или папки, к которому будет применена операция, и *команду* , указывающую операцию.</span><span class="sxs-lookup"><span data-stu-id="9be7d-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="9be7d-115">Для **ShellExecute** присвойте эти значения соответствующим параметрам.</span><span class="sxs-lookup"><span data-stu-id="9be7d-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="9be7d-116">Для **ShellExecuteEx** заполните соответствующие элементы структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9be7d-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="9be7d-117">Существует также несколько других элементов или параметров, которые можно использовать для точной настройки поведения двух функций.</span><span class="sxs-lookup"><span data-stu-id="9be7d-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="9be7d-118">Объекты файлов и папок могут быть частью файловой системы или виртуальных объектов, и их можно идентифицировать по путям или указателям на списки идентификаторов элементов (PIDL).</span><span class="sxs-lookup"><span data-stu-id="9be7d-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="9be7d-119">Команды объекта</span><span class="sxs-lookup"><span data-stu-id="9be7d-119">Object Verbs</span></span>

<span data-ttu-id="9be7d-120">Команды, доступные для объекта, по сути являются элементами, которые находятся в контекстном меню объекта.</span><span class="sxs-lookup"><span data-stu-id="9be7d-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="9be7d-121">Чтобы узнать, какие команды доступны, просмотрите реестр в разделе</span><span class="sxs-lookup"><span data-stu-id="9be7d-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="9be7d-122">**HKey \_ \_Корень классов** \\ **CLSID** \\ *{Object \_ CLSID}* \\  \\ *команда* оболочки</span><span class="sxs-lookup"><span data-stu-id="9be7d-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="9be7d-123">где *\_ CLSID объекта* — это идентификатор класса (CLSID) объекта, а *глагол* — имя доступной команды.</span><span class="sxs-lookup"><span data-stu-id="9be7d-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="9be7d-124">Подключ  \\ **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.</span><span class="sxs-lookup"><span data-stu-id="9be7d-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="9be7d-125">Чтобы узнать, какие команды доступны для [предопределенных объектов оболочки](handlers.md), просмотрите раздел реестра в разделе</span><span class="sxs-lookup"><span data-stu-id="9be7d-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="9be7d-126">**HKey \_ Классы \_ корневого** \\ *объекта \_ имя* класса \\  \\ *команда* оболочки</span><span class="sxs-lookup"><span data-stu-id="9be7d-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="9be7d-127">где *\_ имя объекта* — это имя предопределенного объекта оболочки.</span><span class="sxs-lookup"><span data-stu-id="9be7d-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="9be7d-128">Опять же,  \\ подраздел **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.</span><span class="sxs-lookup"><span data-stu-id="9be7d-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="9be7d-129">Часто доступные команды включают:</span><span class="sxs-lookup"><span data-stu-id="9be7d-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="9be7d-130">Команда</span><span class="sxs-lookup"><span data-stu-id="9be7d-130">Verb</span></span>       | <span data-ttu-id="9be7d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="9be7d-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9be7d-132">изменение;</span><span class="sxs-lookup"><span data-stu-id="9be7d-132">edit</span></span>       | <span data-ttu-id="9be7d-133">Запускает редактор и открывает документ для редактирования.</span><span class="sxs-lookup"><span data-stu-id="9be7d-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="9be7d-134">поиск</span><span class="sxs-lookup"><span data-stu-id="9be7d-134">find</span></span>       | <span data-ttu-id="9be7d-135">Инициирует поиск, начиная с указанного каталога.</span><span class="sxs-lookup"><span data-stu-id="9be7d-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="9be7d-136">open</span><span class="sxs-lookup"><span data-stu-id="9be7d-136">open</span></span>       | <span data-ttu-id="9be7d-137">Запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="9be7d-137">Launches an application.</span></span> <span data-ttu-id="9be7d-138">Если этот файл не является исполняемым файлом, запускается связанное с ним приложение.</span><span class="sxs-lookup"><span data-stu-id="9be7d-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="9be7d-139">print</span><span class="sxs-lookup"><span data-stu-id="9be7d-139">print</span></span>      | <span data-ttu-id="9be7d-140">Выводит файл документа.</span><span class="sxs-lookup"><span data-stu-id="9be7d-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="9be7d-141">properties</span><span class="sxs-lookup"><span data-stu-id="9be7d-141">properties</span></span> | <span data-ttu-id="9be7d-142">Отображает свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="9be7d-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="9be7d-143">запуск от имени</span><span class="sxs-lookup"><span data-stu-id="9be7d-143">runas</span></span>      | <span data-ttu-id="9be7d-144">Запускает приложение от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="9be7d-144">Launches an application as Administrator.</span></span> <span data-ttu-id="9be7d-145">Функция контроля учетных записей (UAC) запросит у пользователя разрешение на запуск приложения с повышенными правами или введите учетные данные администратора, используемого для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="9be7d-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="9be7d-146">Каждая команда соответствует команде, которая будет использоваться для запуска приложения из окна консоли.</span><span class="sxs-lookup"><span data-stu-id="9be7d-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="9be7d-147">Хорошим примером является команда **Open** , так как она обычно поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be7d-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="9be7d-148">Для файлов .exe **Open** просто запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="9be7d-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="9be7d-149">Однако чаще используется для запуска приложения, которое работает с определенным файлом.</span><span class="sxs-lookup"><span data-stu-id="9be7d-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="9be7d-150">Например, файлы .txt могут быть открыты Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="9be7d-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="9be7d-151">Команда **Open** для файла .txt, таким образом, будет соответствовать примерно следующей команде:</span><span class="sxs-lookup"><span data-stu-id="9be7d-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="9be7d-152">При использовании [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для открытия файла .txt Wordpad.exe запускается с указанным файлом в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="9be7d-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="9be7d-153">Некоторые команды могут иметь дополнительные аргументы, например флаги, которые можно добавить при необходимости для правильного запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="9be7d-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="9be7d-154">Дальнейшее обсуждение контекстных меню и глаголов см. в разделе [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="9be7d-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="9be7d-155">Как правило, попытка определить список доступных команд для определенного файла немного сложна.</span><span class="sxs-lookup"><span data-stu-id="9be7d-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="9be7d-156">Во многих случаях можно просто установить для параметра *Лпверб* **значение NULL**, которое вызывает команду по умолчанию для типа файла.</span><span class="sxs-lookup"><span data-stu-id="9be7d-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="9be7d-157">Эта процедура обычно эквивалентна установке *лпверб* в значение "Open", но некоторые типы файлов могут иметь разные команды по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9be7d-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="9be7d-158">Дополнительные сведения см. в разделе [расширение контекстных меню](context.md) и справочная документация по [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="9be7d-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="9be7d-159">Использование ShellExecuteEx для предоставления служб активации с сайта</span><span class="sxs-lookup"><span data-stu-id="9be7d-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="9be7d-160">Службы цепочки сайтов могут управлять множеством поведений активации элементов.</span><span class="sxs-lookup"><span data-stu-id="9be7d-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="9be7d-161">на Windows 8 можно указать указатель на цепочку сайтов, чтобы [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для включения этих поведений.</span><span class="sxs-lookup"><span data-stu-id="9be7d-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="9be7d-162">Чтобы предоставить сайт **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="9be7d-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="9be7d-163">Укажите параметр см \_ \_ . флаг маски \_ хинст \_ — \_ флаг сайта в элементе **фмаск** элемента [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="9be7d-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="9be7d-164">Укажите [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) в члене **хинстапп** объекта [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="9be7d-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="9be7d-165">Использование ShellExecute для запуска диалогового окна поиска</span><span class="sxs-lookup"><span data-stu-id="9be7d-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="9be7d-166">когда пользователь щелкает правой кнопкой мыши значок папки в обозревателе Windows, одним из пунктов меню является «Search» (поиск).</span><span class="sxs-lookup"><span data-stu-id="9be7d-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="9be7d-167">При выборе этого элемента оболочка запускает свою служебную программу поиска.</span><span class="sxs-lookup"><span data-stu-id="9be7d-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="9be7d-168">Эта программа отображает диалоговое окно, которое можно использовать для поиска в файлах указанной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="9be7d-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="9be7d-169">Приложение может программно запустить программу поиска для каталога путем вызова [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)с параметром "Find" в качестве параметра *лпверб* , а путь к каталогу — как параметр *лпфиле* .</span><span class="sxs-lookup"><span data-stu-id="9be7d-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="9be7d-170">Например, следующая строка кода запускает программу поиска для каталога c: \\ мипрограмс.</span><span class="sxs-lookup"><span data-stu-id="9be7d-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="9be7d-171">Простой пример использования ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="9be7d-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="9be7d-172">В следующем примере консольного приложения показано использование [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="9be7d-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="9be7d-173">Для ясности опущена большая часть кода проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="9be7d-173">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="9be7d-174">приложение сначала извлекает пидл каталога Windows и перечисляет его содержимое до тех пор, пока не найдет первый файл .bmp.</span><span class="sxs-lookup"><span data-stu-id="9be7d-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="9be7d-175">В отличие от предыдущего примера, [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) используется для получения имени синтаксического анализа файла вместо его отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="9be7d-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="9be7d-176">Так как это папка файловой системы, имя синтаксического анализа — это полный путь, который необходим для [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="9be7d-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="9be7d-177">После того, как первый файл .bmp найден, соответствующие значения присваиваются элементам структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9be7d-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="9be7d-178">Для элемента **лпфиле** задается имя синтаксического анализа файла, а член **Лпверб** — **значение NULL**, чтобы начать операцию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9be7d-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="9be7d-179">В этом случае по умолчанию используется операция "Открыть".</span><span class="sxs-lookup"><span data-stu-id="9be7d-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="9be7d-180">Структура затем передается в [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), которая запускает обработчик по умолчанию для файлов растрового изображения, обычно MSPaint.exe, чтобы открыть файл.</span><span class="sxs-lookup"><span data-stu-id="9be7d-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="9be7d-181">после возврата функции pidl освобождаются, а интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) папки Windows освобождается.</span><span class="sxs-lookup"><span data-stu-id="9be7d-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 

---
description: После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908744"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="ba7d9-103">Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="ba7d9-104">После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="ba7d9-105">Например, приложению может потребоваться запустить другое приложение, позволяющее пользователю изменять файл данных.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="ba7d9-106">Если файл является исполняемым файлом, приложение может захотеть просто запустить его.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="ba7d9-107">В этом документе описывается, как использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="ba7d9-108">Использование ShellExecute и ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="ba7d9-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="ba7d9-109">Команды объекта</span><span class="sxs-lookup"><span data-stu-id="ba7d9-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="ba7d9-110">Использование ShellExecuteEx для предоставления служб активации с сайта</span><span class="sxs-lookup"><span data-stu-id="ba7d9-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="ba7d9-111">Использование ShellExecute для запуска диалогового окна поиска</span><span class="sxs-lookup"><span data-stu-id="ba7d9-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="ba7d9-112">Простой пример использования ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="ba7d9-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="ba7d9-113">Использование ShellExecute и ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="ba7d9-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="ba7d9-114">Чтобы использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), приложение должно указать объект файла или папки, к которому будет применена операция, и *команду* , указывающую операцию.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="ba7d9-115">Для **ShellExecute** присвойте эти значения соответствующим параметрам.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="ba7d9-116">Для **ShellExecuteEx** заполните соответствующие элементы структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ba7d9-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="ba7d9-117">Существует также несколько других элементов или параметров, которые можно использовать для точной настройки поведения двух функций.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="ba7d9-118">Объекты файлов и папок могут быть частью файловой системы или виртуальных объектов, и их можно идентифицировать по путям или указателям на списки идентификаторов элементов (PIDL).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="ba7d9-119">Команды объекта</span><span class="sxs-lookup"><span data-stu-id="ba7d9-119">Object Verbs</span></span>

<span data-ttu-id="ba7d9-120">Команды, доступные для объекта, по сути являются элементами, которые находятся в контекстном меню объекта.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="ba7d9-121">Чтобы узнать, какие команды доступны, просмотрите реестр в разделе</span><span class="sxs-lookup"><span data-stu-id="ba7d9-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="ba7d9-122">**HKey \_ \_Корень классов** \\ **CLSID** \\ *{Object \_ CLSID}* \\  \\ *команда* оболочки</span><span class="sxs-lookup"><span data-stu-id="ba7d9-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="ba7d9-123">где *\_ CLSID объекта* — это идентификатор класса (CLSID) объекта, а *глагол* — имя доступной команды.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="ba7d9-124">Подключ  \\ **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="ba7d9-125">Чтобы узнать, какие команды доступны для [предопределенных объектов оболочки](handlers.md), просмотрите раздел реестра в разделе</span><span class="sxs-lookup"><span data-stu-id="ba7d9-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="ba7d9-126">**HKey \_ Классы \_ корневого** \\ *объекта \_ имя* класса \\  \\ *команда* оболочки</span><span class="sxs-lookup"><span data-stu-id="ba7d9-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="ba7d9-127">где *\_ имя объекта* — это имя предопределенного объекта оболочки.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="ba7d9-128">Опять же,  \\ подраздел **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="ba7d9-129">Часто доступные команды включают:</span><span class="sxs-lookup"><span data-stu-id="ba7d9-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="ba7d9-130">Команда</span><span class="sxs-lookup"><span data-stu-id="ba7d9-130">Verb</span></span>       | <span data-ttu-id="ba7d9-131">Описание</span><span class="sxs-lookup"><span data-stu-id="ba7d9-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7d9-132">изменение;</span><span class="sxs-lookup"><span data-stu-id="ba7d9-132">edit</span></span>       | <span data-ttu-id="ba7d9-133">Запускает редактор и открывает документ для редактирования.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="ba7d9-134">поиск</span><span class="sxs-lookup"><span data-stu-id="ba7d9-134">find</span></span>       | <span data-ttu-id="ba7d9-135">Инициирует поиск, начиная с указанного каталога.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="ba7d9-136">open</span><span class="sxs-lookup"><span data-stu-id="ba7d9-136">open</span></span>       | <span data-ttu-id="ba7d9-137">Запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-137">Launches an application.</span></span> <span data-ttu-id="ba7d9-138">Если этот файл не является исполняемым файлом, запускается связанное с ним приложение.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="ba7d9-139">print</span><span class="sxs-lookup"><span data-stu-id="ba7d9-139">print</span></span>      | <span data-ttu-id="ba7d9-140">Выводит файл документа.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="ba7d9-141">properties</span><span class="sxs-lookup"><span data-stu-id="ba7d9-141">properties</span></span> | <span data-ttu-id="ba7d9-142">Отображает свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="ba7d9-143">запуск от имени</span><span class="sxs-lookup"><span data-stu-id="ba7d9-143">runas</span></span>      | <span data-ttu-id="ba7d9-144">Запускает приложение от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-144">Launches an application as Administrator.</span></span> <span data-ttu-id="ba7d9-145">Контроль учетных записей (UAC) предложит пользователю подтвердить согласие на</span><span class="sxs-lookup"><span data-stu-id="ba7d9-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="ba7d9-146">Запустите приложение с повышенными правами или введите учетные данные администратора, используемого для запуска</span><span class="sxs-lookup"><span data-stu-id="ba7d9-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="ba7d9-147">приложении Aha!.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="ba7d9-148">Каждая команда соответствует команде, которая будет использоваться для запуска приложения из окна консоли.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="ba7d9-149">Хорошим примером является команда **Open** , так как она обычно поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="ba7d9-150">Для файлов exe программа **Open** просто запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="ba7d9-151">Однако чаще используется для запуска приложения, которое работает с определенным файлом.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="ba7d9-152">Например, файлы. txt могут быть открыты в Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="ba7d9-153">Таким образом, команда **Open** для TXT-файла будет соответствовать примерно следующей команде:</span><span class="sxs-lookup"><span data-stu-id="ba7d9-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="ba7d9-154">При использовании [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для открытия TXT-файла Wordpad.exe запускается с указанным файлом в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="ba7d9-155">Некоторые команды могут иметь дополнительные аргументы, например флаги, которые можно добавить при необходимости для правильного запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="ba7d9-156">Дальнейшее обсуждение контекстных меню и глаголов см. в разделе [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="ba7d9-157">Как правило, попытка определить список доступных команд для определенного файла немного сложна.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="ba7d9-158">Во многих случаях можно просто установить для параметра *Лпверб* **значение NULL**, которое вызывает команду по умолчанию для типа файла.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="ba7d9-159">Эта процедура обычно эквивалентна установке *лпверб* в значение "Open", но некоторые типы файлов могут иметь разные команды по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="ba7d9-160">Дополнительные сведения см. в разделе [расширение контекстных меню](context.md) и справочная документация по [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="ba7d9-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="ba7d9-161">Использование ShellExecuteEx для предоставления служб активации с сайта</span><span class="sxs-lookup"><span data-stu-id="ba7d9-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="ba7d9-162">Службы цепочки сайтов могут управлять множеством поведений активации элементов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="ba7d9-163">Начиная с Windows 8, можно указать указатель на цепочку сайтов, чтобы [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для включения этих поведений.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="ba7d9-164">Чтобы предоставить сайт **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="ba7d9-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="ba7d9-165">Укажите параметр см \_ \_ . флаг маски \_ хинст \_ — \_ флаг сайта в элементе **фмаск** элемента [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="ba7d9-166">Укажите [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) в члене **хинстапп** объекта [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="ba7d9-167">Использование ShellExecute для запуска диалогового окна поиска</span><span class="sxs-lookup"><span data-stu-id="ba7d9-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="ba7d9-168">Когда пользователь щелкает правой кнопкой мыши значок папки в проводнике Windows, один из пунктов меню — «Search» (Поиск).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="ba7d9-169">При выборе этого элемента оболочка запускает свою служебную программу поиска.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="ba7d9-170">Эта программа отображает диалоговое окно, которое можно использовать для поиска в файлах указанной текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="ba7d9-171">Приложение может программно запустить программу поиска для каталога путем вызова [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)с параметром "Find" в качестве параметра *лпверб* , а путь к каталогу — как параметр *лпфиле* .</span><span class="sxs-lookup"><span data-stu-id="ba7d9-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="ba7d9-172">Например, следующая строка кода запускает программу поиска для каталога c: \\ мипрограмс.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="ba7d9-173">Простой пример использования ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="ba7d9-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="ba7d9-174">В следующем примере консольного приложения показано использование [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="ba7d9-175">Для ясности опущена большая часть кода проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-175">Most error checking code has been omitted for clarity.</span></span>


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



<span data-ttu-id="ba7d9-176">Приложение сначала извлекает ПИДЛ каталога Windows и перечисляет его содержимое до тех пор, пока не найдет первый файл. bmp.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="ba7d9-177">В отличие от предыдущего примера, [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) используется для получения имени синтаксического анализа файла вместо его отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="ba7d9-178">Так как это папка файловой системы, имя синтаксического анализа — это полный путь, который необходим для [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="ba7d9-179">После обнаружения первого BMP-файла соответствующие значения присваиваются элементам структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ba7d9-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="ba7d9-180">Для элемента **лпфиле** задается имя синтаксического анализа файла, а член **Лпверб** — **значение NULL**, чтобы начать операцию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="ba7d9-181">В этом случае по умолчанию используется операция "Открыть".</span><span class="sxs-lookup"><span data-stu-id="ba7d9-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="ba7d9-182">Структура затем передается в [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), которая запускает обработчик по умолчанию для файлов растрового изображения, обычно MSPaint.exe, чтобы открыть файл.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="ba7d9-183">После возврата функции PIDL освобождаются и освобождается интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) папки Windows.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 

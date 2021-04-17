---
description: Хранение жестко запрограммированных строк в реестре является частью модели локализации до Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Использование перенаправления строк реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684598"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="a7d3e-103">Использование перенаправления строк реестра</span><span class="sxs-lookup"><span data-stu-id="a7d3e-103">Using Registry String Redirection</span></span>

<span data-ttu-id="a7d3e-104">Хранение жестко запрограммированных строк в реестре является частью модели локализации до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="a7d3e-105">Он не поддерживается многоязыковым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-105">It is not supported by MUI.</span></span> <span data-ttu-id="a7d3e-106">В текущей модели пользовательский интерфейс для операционной системы выполняется в файлах ресурсов, зависящих от языка, поверх базы, не зависящей от языка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="a7d3e-107">Компоненты операционной системы используют реестр независящим от языка способом.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="a7d3e-108">MUI использует только перенаправленные строки реестра, определенные ресурсами Win32 PE в файле ресурсов базового языка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="a7d3e-109">Перенаправление определяется отдельно, например в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="a7d3e-110">Этот тип хранилища позволяет загрузчику ресурсов автоматически выбирать нужные языковые ресурсы при загрузке модуля ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="a7d3e-111">Этот раздел относится только к ресурсам Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="a7d3e-112">При использовании ресурсов, отличных от Win32, при необходимости необходимо указать настраиваемое Перенаправление строки реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="a7d3e-113">Создание Language-Neutral ресурса</span><span class="sxs-lookup"><span data-stu-id="a7d3e-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="a7d3e-114">Приложение MUI, работающее в Windows Vista и более поздних версий, использует строковый ресурс, не зависящий от языка, чтобы предоставить доступ к строкам, относящимся к конкретному языку, хранящимся в таблице строк</span><span class="sxs-lookup"><span data-stu-id="a7d3e-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="a7d3e-115">Код приложения, считывающий эти значения из реестра, описан в разделе Загрузка Language-Neutral значения реестра статьи [Поиск перенаправленных строк](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a7d3e-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="a7d3e-116">Данные для значения реестра, не зависящего от языка, имеют формат " `@<PE-path>,-<stringID>[;<comment>]` ", где:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="a7d3e-117">*PE-Path* указывает путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="a7d3e-118">Для поддержки развертывания можно указать путь, используя переменную среды, например% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="a7d3e-119">Альтернативой для создания ссылки на строку является выход из сведений о пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="a7d3e-120">В этом случае приложение должно иметь некоторые средства, например другое значение реестра, для обмена данными с собственным каталогом установки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="a7d3e-121">*stringID* указывает числовой идентификатор ресурса соответствующего строкового ресурса, который реализуется так же, как любой другой локализуемый строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="a7d3e-122">*Комментарий* указывает дополнительные сведения для отладки или удобства чтения значения реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="a7d3e-123">Функции API реестра игнорируют комментарий при загрузке строки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="a7d3e-124">Данные для значения реестра не имеют явной ссылки на файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="a7d3e-125">Правильный файл определяется во время выполнения в соответствии с текущими предпочтениями языка пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="a7d3e-126">Значение реестра указывается без пробела между "," и "-".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="a7d3e-127">Правильное значение реестра:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="a7d3e-128">Неверное значение реестра:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="a7d3e-129">Примером из Windows Vista является значение реестра со следующими данными:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="a7d3e-130">Создание ресурсов для строк ярлыков</span><span class="sxs-lookup"><span data-stu-id="a7d3e-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="a7d3e-131">Когда приложение MUI отображает имя в пользовательском интерфейсе оболочки, для значка приложения отображается строка подсказки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="a7d3e-132">Для каждого поддерживаемого языка необходимо создать строковые ресурсы для отображаемого имени приложения и соответствующей строки подсказки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="a7d3e-133">Когда ресурсы будут готовы, приложение сможет использовать строки, как описано в разделе Использование API оболочки для загрузки строк ярлыков из раздела реестра [Поиск перенаправленных строк](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a7d3e-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="a7d3e-134">Подготовка ресурсов для ярлыка, созданного с помощью установщик Windows</span><span class="sxs-lookup"><span data-stu-id="a7d3e-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="a7d3e-135">Если для создания ярлыка используется установщик Windows (MSI), строковые ресурсы включают в себя отображаемое имя и описание ярлыка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="a7d3e-136">В [таблице ярлыков MSI](../msi/shortcut-table.md)ссылка на библиотеку ресурсов содержится в соответствующих столбцах, а идентификаторы ресурсов для отображаемого имени и описания ярлыка используются в соответствующих столбцах идентификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="a7d3e-137">Чтобы ярлык приложения правильно работал с технологией ресурсов MUI, учитывайте следующие моменты при подготовке строк ярлыка:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="a7d3e-138">Для регистрации библиотеки DLL используйте либо переменные среды, либо относительный путь.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="a7d3e-139">Можно указать параметр @% systemroot% \\ system32 \\shell32.dll, если строка реестра имеет тип REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="a7d3e-140">Строковый идентификатор ресурса для "текстового документа" в Shell32.dll — 12345.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="a7d3e-141">Не используйте пробелы вокруг символов "," и "-".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="a7d3e-142">Правильный пример: "shell32.dll,-22912".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="a7d3e-143">Не используйте короткое имя файла.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-143">Do not use a short file name.</span></span> <span data-ttu-id="a7d3e-144">Этот тип имени не работает с загрузчиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="a7d3e-145">Подготовка ресурсов для ярлыка с помощью формата INF</span><span class="sxs-lookup"><span data-stu-id="a7d3e-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="a7d3e-146">Если для создания строк ярлыков используется формат файла INF, файл ресурсов должен иметь следующие параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="a7d3e-147">В этих инструкциях предполагается использование синтаксиса Профилеитемс API установки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="a7d3e-148">Измените значение подсказки, чтобы оно указывало на ссылку перенаправления строк, используя путь и идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="a7d3e-149">Добавьте новое значение Дисплайресаурце в разделы установки Профилеитемс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="a7d3e-150">Ниже приведен пример добавления приложения Calculator в меню **Пуск** .</span><span class="sxs-lookup"><span data-stu-id="a7d3e-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="a7d3e-151">Используйте синтаксис, показанный ниже, при использовании INF-файла для добавления элементов, например, папки группы доступа, в меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="a7d3e-152">Этот синтаксис предполагает использование \[ \] поддержки Стартменуитемс из программы установки аналогично синтаксису, используемому в сиссетуп. INF.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="a7d3e-153">Задайте в *подсказке* значения ссылку на строку " `@<path>,-resID` ".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="a7d3e-154">Отображаемое имя определяется значениями *ресдлл* и *resID* .</span><span class="sxs-lookup"><span data-stu-id="a7d3e-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="a7d3e-155">Значение *resID* указывает идентификатор ресурса для строкового ресурса, связанного с файлом, не зависящим от языка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="a7d3e-156">Значение *ресдлл* указывает путь к файлу, не зависящему от языка.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="a7d3e-157">Создание ресурсов для понятных имен типов документов</span><span class="sxs-lookup"><span data-stu-id="a7d3e-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="a7d3e-158">Необходимо реализовать понятные имена и строки подсказки для приложения в качестве строковых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="a7d3e-159">Чтобы разрешить дружественные имена типов документов для реагирования на язык пользовательского интерфейса, приложение должно зарегистрировать имена с помощью значения Фриендлитипенаме в ключе идентификатора программы для типа файла.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="a7d3e-160">Значение по умолчанию для ключа идентификатора программы должно быть сохранены для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="a7d3e-161">Сведения о доступе к именам из приложения см. в разделе "запрос понятных имен типов документов" раздела реестра [Поиск перенаправленных строк](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a7d3e-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="a7d3e-162">Конкретная работа состоит из следующих этапов.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="a7d3e-163">Реализуйте понятное имя и строки подсказки в качестве строковых ресурсов для конкретных языков.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="a7d3e-164">Добавьте значение Фриендлитипенаме в раздел реестра типа документа.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="a7d3e-165">Данные для значения следуют шаблону " `@<path>,-<resID>` ", где *path* указывает исполняемый файл, а *resID* — идентификатор ресурса локализуемого строкового ресурса, связанного с этим исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="a7d3e-166">Укажите значение реестра подсказки в формате " `@<path>,-<resID>` ".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="a7d3e-167">В следующем примере показаны параметры реестра для TXT-файла.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="a7d3e-168">Предоставление ресурсов для строк действий команд оболочки</span><span class="sxs-lookup"><span data-stu-id="a7d3e-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="a7d3e-169">Строки действий для определенных команд, например "Открыть" и "Изменить", отображаются во всплывающем меню, которое отображается, когда пользователь щелкает правой кнопкой мыши файл в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="a7d3e-170">Приложению не нужно указывать строки для общих команд оболочки, так как оболочка имеет собственные параметры по умолчанию, поддерживающие MUI для этих команд.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="a7d3e-171">Однако необходимо предоставить локализуемые строковые ресурсы для строк, представляющих нестандартные команды.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="a7d3e-172">В операционных системах, предшествующих Windows XP, строки для команд оболочки в реестре подготавливаются к просмотру с помощью следующего синтаксиса, где *команда* указывает фактическое имя команды:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="a7d3e-173">Приведем пример:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="a7d3e-174">В Windows XP и более поздних версиях можно использовать уровень косвенного обращения для того, чтобы строка действия зависела от языка пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="a7d3e-175">Эти операционные системы поддерживают значение Муиверб для определения строки, совместимой с MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="a7d3e-176">Ниже приведен пример записи реестра для нестандартной команды:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="a7d3e-177">Приложение MUI также должно иметь возможность зарегистрировать старое значение по умолчанию как локализуемое строку, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="a7d3e-178">Регистрация старого значения по умолчанию не рекомендуется, так как для нее требуется другая программа установки Windows XP и более поздней версии из программы установки, которая использовалась в предыдущих версиях операционных систем.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="a7d3e-179">Создание ресурсов для строк глагола, протокола и Ауксусертипе</span><span class="sxs-lookup"><span data-stu-id="a7d3e-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="a7d3e-180">Необходимо создать локализуемые строковые ресурсы для глаголов, протоколов и строк Ауксусертипе.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="a7d3e-181">Используйте следующие параметры реестра:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="a7d3e-182">Значение, указанное для Локализедстринг, содержит или заменяет значение для *команды*, а не два значения флага.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="a7d3e-183">Ниже приведена сводка по обеспечению правильных настроек реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="a7d3e-184">Если у CLSID есть \\ ключ CLSID \\ (CLSID \\ ) с ключом HKCR, определите значение по умолчанию CLSID, используя HKCR \\ CLSID \\ {CLSID} \\ локализедстринг.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="a7d3e-185">Если у CLSID есть один или несколько подразделов \\ в \\ команде HKCR CLSID {CLSID} \\ , определите каждую отдельную строку команды с помощью \\ команды HKCR CLSID \\ {CLSID} \\ \\ \\ локализедстринг.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="a7d3e-186">Если у CLSID есть один или несколько подразделов в \\ команде HKCR {ProgID} \\ Protocol \\ стдфилидитинг \\ , определите каждую отдельную строку команды с помощью \\ команды HKCR {ProgID} \\ \\ стдфилидитинг протокола \\ \\ xxx \\ локализедстринг.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="a7d3e-187">Если в CLSID имеется один или несколько перечисленных подразделов Ауксусертипе в разделе HKCR \\ CLSID \\ {CLSID} \\ ауксусертипе, определите каждую запись АУКСУСЕРТИПЕ с помощью HKCR \\ CLSID \\ {CLSID} \\ ауксусертипе \\ xxx \\ локализедстринг.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="a7d3e-188">Создание ресурса для программы удаления</span><span class="sxs-lookup"><span data-stu-id="a7d3e-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="a7d3e-189">Чтобы зарегистрировать программу удаления для приложения, можно создать значения реестра в подразделе уникальный идентификатор для приложения в разделе реестра HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ uninstall.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="a7d3e-190">Значения для установки включают: DisplayName, Дисплайверсион, Publisher, ProductID, Реговнер, Регкомпани, Урлинфоабаут, Хелптелефоне, HelpLink, InstallLocation, Инсталлсаурце, Инсталлдате, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="a7d3e-191">Чтобы включить технологию MUI для каждого значения, можно добавить " \_ локализованный" к имени значения.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="a7d3e-192">Компоненты операционной системы необходимы для предоставления значения для DisplayName, \_ локализованного в соответствии с MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="a7d3e-193">Необходимо поместить отображаемое имя в библиотеку DLL, например Res.dll, в виде строкового ресурса, предполагая, что идентификатор 1245.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="a7d3e-194">Затем приложение может зарегистрировать отображаемое имя как DisplayName, \_ локализованное со значением "@ \\res.DLL,-1245".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="a7d3e-195">Все остальные параметры реестра должны быть сохранены, включая исходное значение DisplayName.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="a7d3e-196">Создание ресурсов для событий звука</span><span class="sxs-lookup"><span data-stu-id="a7d3e-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="a7d3e-197">Windows связывает определенные события с звуковыми файлами, например с уведомлением о новом сообщении электронной почты или событием предупреждения о критическом аккумуляторе.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="a7d3e-198">Имена событий должны отображаться в пользовательском интерфейсе и должны поддерживать глобализацию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="a7d3e-199">Поэтому следует реализовать локализуемый строковый ресурс для описания каждого описания события.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="a7d3e-200">Добавьте новое значение реестра для каждого имени события в дополнение к жестко запрограммированному значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="a7d3e-201">Чтобы включить звуковое событие, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="a7d3e-202">Реализуйте описание как локализуемый строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="a7d3e-203">Добавьте новое значение реестра для отображаемого имени в дополнение к жестко запрограммированному значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="a7d3e-204">Ниже показан соответствующий макет реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="a7d3e-205">Если оболочке не удается найти или получить значение Диспфиленаме, используется описание по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="a7d3e-206">Создание ресурсов для строк раскладки клавиатуры</span><span class="sxs-lookup"><span data-stu-id="a7d3e-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="a7d3e-207">Если приложение реализует раскладку клавиатуры, для отображения имени макета экрана, например, в списках раскладок клавиатуры требуется локализуемый строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="a7d3e-208">У каждой раскладки клавиатуры есть раздел реестра в разделе HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ LAYOUTS.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="a7d3e-209">Значениями для этого ключа являются текст макета, удобное для чтения имя для обратной совместимости и отображаемое имя макета.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="a7d3e-210">Данные, передаваемые для отображаемого имени макета, должны быть строковой ссылкой в форме " `@<path>,-resID` ", ссылающейся на локализуемый строковый ресурс, связанный с раскладкой клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="a7d3e-211">Ниже приведен пример параметра реестра для раскладки клавиатуры "Испанский (Испания)":</span><span class="sxs-lookup"><span data-stu-id="a7d3e-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="a7d3e-212">Представление строк общих диалоговых окон вставки объекта OLE</span><span class="sxs-lookup"><span data-stu-id="a7d3e-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="a7d3e-213">Отображаемое имя вставляемого объекта OLE можно реализовать как локализуемый строковый ресурс, связанный с кодом, реализующим этот объект.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="a7d3e-214">[Диалоговое окно OLE: Вставка объекта](/cpp/mfc/reference/coleinsertdialog-class) получает отображаемое имя из раздела реестра HKCR \\ CLSID \\ { *<GUID>* }, где *GUID* определяет идентификатор класса вставляемого объекта OLE.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="a7d3e-215">Windows Vista и более поздние версии реализуют этот тип объектов в локализуемых способах, используя отображаемое имя, совместимое с MUI, которое позволяет настраивать язык пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="a7d3e-216">В отличие от этого, операционные системы предыдущих версий Windows Vista реализуют отображаемое имя для этого типа объекта, используя значение по умолчанию соответствующего раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="a7d3e-217">Обычно это имя является либо именем английского (США), либо именем в системном языке пользовательского интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="a7d3e-218">Не все объекты, соответствующие подразделам раздела реестра, можно вставлять.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="a7d3e-219">Значение по умолчанию \\ \\ ключа CLSID { *<GUID>* } раздела HKCR должно содержать удобное для чтения имя для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="a7d3e-220">Однако он также должен определять значение Локализедстринг в формате " `@<path>,-ResID` ", где путь определяет исполняемый файл, реализующий объект.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="a7d3e-221">Значение ResID указывает идентификатор ресурса локализуемой строки для отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="a7d3e-222">Например, скрипт регистрации для вставляемого объекта клипа мультимедиа содержит следующие строки:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="a7d3e-223">Первая строка обеспечивает обратную совместимость, помещая в реестре простую текстовую строку в качестве отображаемого имени по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="a7d3e-224">Вторая строка предоставляет доступ к отображаемому имени, совместимому с MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="a7d3e-225">Указывает идентификатор строки, хранящийся в Mplay32.exe.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="a7d3e-226">Строку с идентификатором 9217 в Mplay32.exe можно связать со строковыми значениями ресурсов для любого числа языков.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="a7d3e-227">Название английского языка (США) — "клип мультимедиа".</span><span class="sxs-lookup"><span data-stu-id="a7d3e-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="a7d3e-228">Создание строковых ресурсов для консоли управления (Майкрософт) Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="a7d3e-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="a7d3e-229">Необходимо создать локализуемый строковый ресурс для каждой оснастки консоли управления (MMC), используемой приложением MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="a7d3e-230">Поскольку оснастка является частью консоли, она имеет пользовательский интерфейс и должна быть глобализована для работы на более чем одном языке.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="a7d3e-231">В большинстве случаев оснастки MMC вызывают те же проблемы глобализации и локализации, что и само приложение MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="a7d3e-232">Оснастка MMC должна отражать свое имя в реестре для отображения.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="a7d3e-233">Запись реестра должна включать косвенную ссылку на локализуемый строковый ресурс и литеральную строку для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="a7d3e-234">Каждая оснастка консоли управления (MMC) содержит раздел реестра в разделе HKEY \_ Local \_ Machine \\ Software \\ Microsoft \\ MMC \\ оснастки.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="a7d3e-235">В качестве значения для этого ключа можно указать Наместринг, указав удобное для чтения имя для обратной совместимости и Наместрингиндирект, указав косвенную ссылку на локализуемый строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="a7d3e-236">Для Наместрингиндирект необходимо предоставить ссылку на строку в форме " `@<path>,-resID` ", представляющую локализуемый строковый ресурс.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="a7d3e-237">Например, можно настроить следующий параметр для Mymmc.dll, где 12345 — идентификатор соответствующего строкового ресурса, содержащего локализуемое имя оснастки:</span><span class="sxs-lookup"><span data-stu-id="a7d3e-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="a7d3e-238">Некоторые оснастки регистрируют другие строковые значения реестра, которые MMC не считывает из реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="a7d3e-239">Дополнительные сведения об использовании этих значений см. в разделе Регистрация [перенаправленных строк](locating-redirected-strings.md)консоли управления Microsoft Snap-In строк, не считанных из реестра.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="a7d3e-240">Создание строковых ресурсов для службы Windows</span><span class="sxs-lookup"><span data-stu-id="a7d3e-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="a7d3e-241">Хотя служба Windows обычно имеет небольшую или не имеющую пользовательский интерфейс, она должна отображать имя, совместимое с MUI, и обычно содержит описание, совместимое с MUI.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="a7d3e-242">Раздел реестра, описывающий службу Windows, поддерживает только значение DisplayName для имени службы и значение описания службы.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="a7d3e-243">Параметры для службы Windows выполняются из приложения, как описано в статье Установка отображаемого имени и описания для службы Windows из реестра в разделе [Поиск перенаправленных строк](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a7d3e-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="a7d3e-244">Если в приложении не заданы значения реестра для пользовательского интерфейса службы, значения в реестре остаются установленными на английском языке, даже если пользовательский интерфейс находится на другом языке.</span><span class="sxs-lookup"><span data-stu-id="a7d3e-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7d3e-245">См. также</span><span class="sxs-lookup"><span data-stu-id="a7d3e-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d3e-246">Подготовка ресурсов</span><span class="sxs-lookup"><span data-stu-id="a7d3e-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="a7d3e-247">Поиск перенаправленных строк</span><span class="sxs-lookup"><span data-stu-id="a7d3e-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 

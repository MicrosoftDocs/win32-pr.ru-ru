---
description: Для элементов панели управления, реализованных в виде EXE-файлов, Специальные операции экспорта или обработки сообщений не требуются. Любой exe-файл можно зарегистрировать в качестве объекта команды, который будет отображаться с точкой входа в папке панели управления.
title: Регистрация исполняемых элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080772"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="577d1-104">Регистрация исполняемых элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="577d1-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="577d1-105">Для элементов панели управления, реализованных в виде EXE-файлов, Специальные операции экспорта или обработки сообщений не требуются.</span><span class="sxs-lookup"><span data-stu-id="577d1-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="577d1-106">Любой exe-файл можно зарегистрировать в качестве объекта команды, который будет отображаться с точкой входа в папке панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="577d1-107">Пример используется для демонстрации требований к регистрации.</span><span class="sxs-lookup"><span data-stu-id="577d1-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="577d1-108">В примере показано, как зарегистрировать элемент панели управления с именем **My Settings** в качестве объекта команды, чтобы он появился в окне панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="577d1-109">Окно **Мои параметры** также появляется при `MyApp.exe /settings` выполнении команды.</span><span class="sxs-lookup"><span data-stu-id="577d1-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="577d1-110">Инструкции</span><span class="sxs-lookup"><span data-stu-id="577d1-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="577d1-111">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="577d1-111">Step 1:</span></span>

<span data-ttu-id="577d1-112">Создайте идентификатор GUID для элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="577d1-113">Идентификатор GUID однозначно определяет элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="577d1-114">В этом примере `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` — это идентификатор GUID элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="577d1-115">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="577d1-115">Step 2:</span></span>

<span data-ttu-id="577d1-116">Используя идентификатор GUID в качестве имени, добавьте подраздел в реестр следующим образом.</span><span class="sxs-lookup"><span data-stu-id="577d1-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="577d1-117">Данные для записи по умолчанию — это просто \_ имя REG SZ элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="577d1-118">Запись по умолчанию может оказаться полезной для поиска идентификатора GUID, но это необязательно.</span><span class="sxs-lookup"><span data-stu-id="577d1-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="577d1-119">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="577d1-119">Step 3:</span></span>

<span data-ttu-id="577d1-120">Используя идентификатор GUID в качестве имени, добавьте подраздел и его записи в реестр, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="577d1-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="577d1-121">**Default**.</span><span class="sxs-lookup"><span data-stu-id="577d1-121">**Default**.</span></span> <span data-ttu-id="577d1-122">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-122">REG\_SZ.</span></span> <span data-ttu-id="577d1-123">Отображаемое имя для элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="577d1-124">**Локализедстринг**.</span><span class="sxs-lookup"><span data-stu-id="577d1-124">**LocalizedString**.</span></span> <span data-ttu-id="577d1-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="577d1-125">Optional.</span></span> <span data-ttu-id="577d1-126">REG \_ SZ или REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="577d1-127">Имя модуля и идентификатор таблицы строк локализованного имени элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="577d1-128">Формат представляет собой знак "at" (@), за которым следует имя EXE-или DLL-файла, содержащего таблицу строк многоязыкового пользовательского интерфейса (MUI).</span><span class="sxs-lookup"><span data-stu-id="577d1-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="577d1-129">Переменные среды можно использовать в качестве замены части пути.</span><span class="sxs-lookup"><span data-stu-id="577d1-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="577d1-130">В пути и имени файла следует запятая (,) и дефис (-), за которым следует идентификатор в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="577d1-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="577d1-131">Если у модуля нет таблицы строк, то эта запись может просто быть отображаемой строкой имени.</span><span class="sxs-lookup"><span data-stu-id="577d1-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="577d1-132">При использовании только строки отображаемого имени, а не таблицы строк, имя не изменяется на текущий язык интерфейса.</span><span class="sxs-lookup"><span data-stu-id="577d1-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="577d1-133">**Подсказка**.</span><span class="sxs-lookup"><span data-stu-id="577d1-133">**InfoTip**.</span></span> <span data-ttu-id="577d1-134">REG \_ SZ или REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="577d1-135">Описание элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-135">A description of the Control Panel item.</span></span> <span data-ttu-id="577d1-136">Эта информация отображается во всплывающей подсказке, которая отображается при наведении указателя мыши на значок элемента.</span><span class="sxs-lookup"><span data-stu-id="577d1-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="577d1-137">Синтаксис такой же, как и для Локализедстринг, включая возможность простого предоставления строки, а не ссылки на таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="577d1-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="577d1-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="577d1-138">**System.ApplicationName**.</span></span> <span data-ttu-id="577d1-139">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-139">REG\_SZ.</span></span> <span data-ttu-id="577d1-140">Каноническое имя элемента.</span><span class="sxs-lookup"><span data-stu-id="577d1-140">The canonical name of the item.</span></span> <span data-ttu-id="577d1-141">Команда формы `control.exe /name System.ApplicationName` открывает элемент, например `control.exe /name MyCorporation.MySettings` .</span><span class="sxs-lookup"><span data-stu-id="577d1-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="577d1-142">Дополнительные сведения об использовании Control.exe см. в разделе [исполнение элементов панели управления](executing-control-panel-items.md) .</span><span class="sxs-lookup"><span data-stu-id="577d1-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="577d1-143">**System. контролпанел. Category**.</span><span class="sxs-lookup"><span data-stu-id="577d1-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="577d1-144">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-144">REG\_SZ.</span></span> <span data-ttu-id="577d1-145">Значение, объявляющее категории панели управления, в которых отображается элемент.</span><span class="sxs-lookup"><span data-stu-id="577d1-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="577d1-146">Несколько категорий разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="577d1-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="577d1-147">В приведенном выше примере запись указывает, что элемент " **Мои параметры** " должен отображаться в категориях "внешний вид", " **Персонализация** " и " **программы** ".</span><span class="sxs-lookup"><span data-stu-id="577d1-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="577d1-148">См. раздел [Назначение категорий панели управления](assigning-control-panel-categories.md) для возможных значений категорий.</span><span class="sxs-lookup"><span data-stu-id="577d1-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="577d1-149">**System. Software. тасксфилеурл**.</span><span class="sxs-lookup"><span data-stu-id="577d1-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="577d1-150">REG \_ SZ или REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="577d1-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="577d1-151">Путь к XML-файлу, который определяет [связи задач](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="577d1-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="577d1-152">Это может быть прямой путь к файлу, как показано в примере, или внедренный ресурс, указанный в качестве имени модуля, и идентификатор ресурса, например "% ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".</span><span class="sxs-lookup"><span data-stu-id="577d1-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="577d1-153">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="577d1-153">Step 4:</span></span>

<span data-ttu-id="577d1-154">В том же подразделе GUID добавьте следующий подраздел в реестр, чтобы указать путь к файлу, содержащему значок, и идентификатор ресурса изображения в этом файле.</span><span class="sxs-lookup"><span data-stu-id="577d1-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="577d1-155">Обратите внимание, что хотя синтаксис похож на упомянутые выше записи Локализедстринг и подсказки, в качестве префикса в записи REG SZ или REG Expand не используется символ "@" \_ \_ \_ , указывающий путь.</span><span class="sxs-lookup"><span data-stu-id="577d1-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="577d1-156">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="577d1-156">Step 5:</span></span>

<span data-ttu-id="577d1-157">Добавьте следующие сведения в реестр для предоставления команды, вызываемой системой при открытии пользователем панели управления.</span><span class="sxs-lookup"><span data-stu-id="577d1-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="577d1-158">См. также</span><span class="sxs-lookup"><span data-stu-id="577d1-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577d1-159">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="577d1-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="577d1-160">Регистрация элементов панели управления DLL</span><span class="sxs-lookup"><span data-stu-id="577d1-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 




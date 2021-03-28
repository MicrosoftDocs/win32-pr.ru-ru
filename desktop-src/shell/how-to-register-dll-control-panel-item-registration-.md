---
description: Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию Кплапплет, имеют различные требования к регистрации, чем exe-файлы.
title: Регистрация элементов панели управления DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813697"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="3786f-103">Регистрация элементов панели управления DLL</span><span class="sxs-lookup"><span data-stu-id="3786f-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="3786f-104">Текущие рекомендации по реализации содержат новые элементы панели управления, которые должны быть реализованы в виде exe, а не файлов. cpl.</span><span class="sxs-lookup"><span data-stu-id="3786f-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="3786f-105">Приведенная ниже информация включается в основном для устаревших целей.</span><span class="sxs-lookup"><span data-stu-id="3786f-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="3786f-106">Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) , имеют различные требования к регистрации, чем exe-файлы.</span><span class="sxs-lookup"><span data-stu-id="3786f-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="3786f-107">Начиная с Windows XP, новые библиотеки элементов панели управления должны быть установлены в папку соответствующего приложения в папке Program Files.</span><span class="sxs-lookup"><span data-stu-id="3786f-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="3786f-108">Не обязательно регистрировать элементы, хранящиеся в каталоге System32 с расширением. cpl; они автоматически отображаются на панели управления.</span><span class="sxs-lookup"><span data-stu-id="3786f-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="3786f-109">Все остальные элементы панели управления, использующие **кплапплет** , должны быть зарегистрированы одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="3786f-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="3786f-110">Если элемент панели управления должен быть доступен всем пользователям, зарегистрируйте путь для каждого компьютера, добавив параметр **reg \_ expand \_ SZ** в раздел **hKey \_ Local \_ Machine** \\ **Software** \\  \\  \\  \\ **панели управления** Microsoft Windows CurrentVersion \\ **CPLS** , указав путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="3786f-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="3786f-111">Если элемент панели управления должен быть доступен отдельно для каждого пользователя, используйте раздел **hKey \_ текущий \_ пользователь** в качестве корневого ключа вместо **\_ локального \_ компьютера hKey**.</span><span class="sxs-lookup"><span data-stu-id="3786f-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="3786f-112">В следующих двух примерах регистрируется элемент панели управления *микплапп* .</span><span class="sxs-lookup"><span data-stu-id="3786f-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="3786f-113">Библиотека DLL называется MyCpl.cpl и находится в каталоге приложения *MyCorp \\ MyApp* .</span><span class="sxs-lookup"><span data-stu-id="3786f-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="3786f-114">В первом примере демонстрируется регистрация на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3786f-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="3786f-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="3786f-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="3786f-116">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="3786f-116">Step 1:</span></span>

<span data-ttu-id="3786f-117">Добавьте эти сведения в реестр для регистрации существования файла. cpl.</span><span class="sxs-lookup"><span data-stu-id="3786f-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="3786f-118">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="3786f-118">Step 2:</span></span>

<span data-ttu-id="3786f-119">**Windows Vista и более поздние версии:** Добавьте эти дополнительные сведения в реестр, чтобы предоставить идентификатор GUID для элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="3786f-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="3786f-120">Создавая идентификатор GUID для уникальной идентификации элемента панели управления, можно добавить ссылки задач в панель управления.</span><span class="sxs-lookup"><span data-stu-id="3786f-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="3786f-121">Без этого GUID ссылки на задачи не будут связаны с элементом панели управления.</span><span class="sxs-lookup"><span data-stu-id="3786f-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="3786f-122">См. раздел [Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="3786f-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="3786f-123">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="3786f-123">Step 3:</span></span>

<span data-ttu-id="3786f-124">**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр, чтобы создать каноническое имя для элемента.</span><span class="sxs-lookup"><span data-stu-id="3786f-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="3786f-125">Добавляя каноническое имя, пользователи могут запускать элемент панели управления из командной строки, вводя `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="3786f-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="3786f-126">Это также позволяет изменить реализацию из CPL-файла на exe-файл, не требуя от программы вызывать какие-либо изменения, так как они могут продолжить открытие элемента по его каноническому имени.</span><span class="sxs-lookup"><span data-stu-id="3786f-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="3786f-127">Дополнительные сведения об канонических именах см. в разделе [исполнение элементов панели управления](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="3786f-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="3786f-128">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="3786f-128">Step 4:</span></span>

<span data-ttu-id="3786f-129">**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр, чтобы назначить элемент панели управления одной или нескольким категориям.</span><span class="sxs-lookup"><span data-stu-id="3786f-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="3786f-130">**Windows XP:** Добавьте следующие сведения в реестр, чтобы назначить элемент панели управления одной или нескольким категориям.</span><span class="sxs-lookup"><span data-stu-id="3786f-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="3786f-131">В этом примере элемент назначается категории 3, которая является сетью и Интернетом.</span><span class="sxs-lookup"><span data-stu-id="3786f-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="3786f-132">Чтобы добавить элемент в несколько категорий, укажите в качестве \_ значения reg SZ значение, разделенное запятыми, например "3, 8".</span><span class="sxs-lookup"><span data-stu-id="3786f-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="3786f-133">Значения могут быть указаны в виде десятичного или шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="3786f-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="3786f-134">Обратите внимание, что возможность добавления элемента в несколько категорий возможна только в Windows XP с пакетом обновления 2 (SP2) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3786f-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="3786f-135">См. раздел [Назначение категорий панели управления](assigning-control-panel-categories.md) для всех возможных значений.</span><span class="sxs-lookup"><span data-stu-id="3786f-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="3786f-136">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="3786f-136">Step 5:</span></span>

<span data-ttu-id="3786f-137">**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр для создания и наведите указатель на XML-файл, содержащий ссылки на задачи для данного элемента.</span><span class="sxs-lookup"><span data-stu-id="3786f-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="3786f-138">Значение должно представлять собой \_ путь к reg-SZ, как показано здесь, а также модуль и идентификатор ресурса (например, "C: \\ Program Files \\ MyCorp \\ MyApp \\MyApp.exe,-31"), если это внедренный ресурс.</span><span class="sxs-lookup"><span data-stu-id="3786f-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="3786f-139">Расположение XML-файла должно быть указано полностью.</span><span class="sxs-lookup"><span data-stu-id="3786f-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="3786f-140">Он не может использовать переменную среды, например% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="3786f-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="3786f-141">Дополнительные сведения о связях задач и о создании XML-файла для их хранения см. [в разделе Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="3786f-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3786f-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3786f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3786f-143">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="3786f-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="3786f-144">Регистрация исполняемых элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="3786f-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 

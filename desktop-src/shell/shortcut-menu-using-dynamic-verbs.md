---
description: Обработчики контекстного меню также известны как обработчики контекстного меню или обработчики команд. Обработчик контекстного меню — это тип обработчика типа файлов.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Настройка контекстного меню с помощью динамических команд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985752"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="14ff3-104">Настройка контекстного меню с помощью динамических команд</span><span class="sxs-lookup"><span data-stu-id="14ff3-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="14ff3-105">Обработчики контекстного меню также известны как обработчики контекстного меню или обработчики команд.</span><span class="sxs-lookup"><span data-stu-id="14ff3-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="14ff3-106">Обработчик контекстного меню — это тип обработчика типа файлов.</span><span class="sxs-lookup"><span data-stu-id="14ff3-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="14ff3-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14ff3-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="14ff3-108">О статических и динамических командах</span><span class="sxs-lookup"><span data-stu-id="14ff3-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="14ff3-109">Работа обработчиков контекстного меню с динамическими командами</span><span class="sxs-lookup"><span data-stu-id="14ff3-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="14ff3-110">Предотвращение конфликтов из-за неуточненных имен команд</span><span class="sxs-lookup"><span data-stu-id="14ff3-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="14ff3-111">Регистрация обработчика контекстного меню с динамической командой</span><span class="sxs-lookup"><span data-stu-id="14ff3-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="14ff3-112">Реализация интерфейса IContextMenu</span><span class="sxs-lookup"><span data-stu-id="14ff3-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="14ff3-113">Метод IContextMenu:: Жеткоммандстринг</span><span class="sxs-lookup"><span data-stu-id="14ff3-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="14ff3-114">Метод IContextMenu:: Инвокекомманд</span><span class="sxs-lookup"><span data-stu-id="14ff3-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="14ff3-115">Метод IContextMenu:: Куериконтекстмену</span><span class="sxs-lookup"><span data-stu-id="14ff3-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="14ff3-116">См. также</span><span class="sxs-lookup"><span data-stu-id="14ff3-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="14ff3-117">О статических и динамических командах</span><span class="sxs-lookup"><span data-stu-id="14ff3-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="14ff3-118">Мы настоятельно рекомендуем реализовать контекстное меню с помощью одного из статических методов глагола.</span><span class="sxs-lookup"><span data-stu-id="14ff3-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="14ff3-119">Рекомендуется следовать инструкциям, приведенным в разделе "Настройка контекстного меню с помощью статических глаголов" раздела [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="14ff3-120">Чтобы получить динамическое поведение для статических глаголов в Windows 7 и более поздних версиях, см. раздел «получение динамического поведения для статических глаголов» раздела [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="14ff3-121">Дополнительные сведения о реализации статических команд и о том, какие динамические команды следует избегать, см. в разделе [Выбор статической или динамической команды для контекстного меню](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="14ff3-122">Если необходимо расширить контекстное меню для типа файла, зарегистрировав динамическую команду для типа файла, следуйте инструкциям, приведенным далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="14ff3-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="14ff3-123">При регистрации обработчиков, работающих в контексте 32-разрядных приложений, существуют особые рекомендации для 64-разрядных систем: при вызове команд оболочки в контексте 32-разрядного приложения Подсистема WOW64 перенаправляет доступ к некоторым путям в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="14ff3-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="14ff3-124">Если обработчик. exe хранится в одном из этих путей, он недоступен в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="14ff3-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="14ff3-125">Поэтому в качестве решения сохраните EXE-файл в пути, который не перенаправлен, или сохраните версию заглушки exe-файла, которая запускает реальную версию.</span><span class="sxs-lookup"><span data-stu-id="14ff3-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="14ff3-126">Работа обработчиков контекстного меню с динамическими командами</span><span class="sxs-lookup"><span data-stu-id="14ff3-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="14ff3-127">Помимо [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), обработчики контекстного меню экспортируют следующие дополнительные интерфейсы для обработки обмена сообщениями, необходимого для реализации элементов меню, рисуемых владельцем.</span><span class="sxs-lookup"><span data-stu-id="14ff3-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="14ff3-128">[**Ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (обязательный)</span><span class="sxs-lookup"><span data-stu-id="14ff3-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="14ff3-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (обязательный)</span><span class="sxs-lookup"><span data-stu-id="14ff3-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="14ff3-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14ff3-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="14ff3-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14ff3-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="14ff3-132">Дополнительные сведения об элементах меню, рисуемых владельцем, см. в разделе *создание Owner-Drawn пунктов меню* раздела [Использование меню](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="14ff3-133">Оболочка использует интерфейс [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) для инициализации обработчика.</span><span class="sxs-lookup"><span data-stu-id="14ff3-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="14ff3-134">Когда оболочка вызывает [**ишеллекстинит:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), она передает объект данных с именем объекта и указателем на список идентификаторов элементов (Пидл) папки, содержащей файл.</span><span class="sxs-lookup"><span data-stu-id="14ff3-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="14ff3-135">Параметр *хкэйпрогид* — это расположение реестра, в котором зарегистрирован маркер контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="14ff3-136">Метод **ишеллекстинит:: Initialize** должен извлечь имя файла из объекта данных и сохранить имя и указатель папки в списке идентификаторов элементов (Пидл) для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="14ff3-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="14ff3-137">Дополнительные сведения об инициализации обработчика см. в разделе [Реализация ишеллекстинит](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="14ff3-138">Когда глаголы представлены в контекстном меню, они сначала обнаруживаются, затем представляются пользователю, и, наконец, вызываются.</span><span class="sxs-lookup"><span data-stu-id="14ff3-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="14ff3-139">В следующем списке приведено более подробное описание этих трех шагов.</span><span class="sxs-lookup"><span data-stu-id="14ff3-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="14ff3-140">Оболочка вызывает метод [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), возвращающий набор команд, которые могут основываться на состоянии элементов или системы.</span><span class="sxs-lookup"><span data-stu-id="14ff3-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="14ff3-141">Система передает в **HMENUный** обработчик, который метод может использовать для добавления элементов в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="14ff3-142">Если пользователь щелкает один из элементов обработчика, оболочка вызывает [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="14ff3-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="14ff3-143">Затем обработчик может выполнить соответствующую команду.</span><span class="sxs-lookup"><span data-stu-id="14ff3-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="14ff3-144">Предотвращение конфликтов из-за неуточненных имен команд</span><span class="sxs-lookup"><span data-stu-id="14ff3-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="14ff3-145">Так как глаголы зарегистрированы для каждого типа, одно и то же имя команды можно использовать для глаголов в различных элементах.</span><span class="sxs-lookup"><span data-stu-id="14ff3-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="14ff3-146">Это позволяет приложениям ссылаться на общие глаголы независимо от типа элемента.</span><span class="sxs-lookup"><span data-stu-id="14ff3-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="14ff3-147">Хотя эта функция полезна, использование неквалифицированных имен может привести к конфликтам с несколькими независимыми поставщиками программного обеспечения (ISV), которые выбирают одно и то же имя команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="14ff3-148">Чтобы избежать этого, всегда добавляйте перед глаголами имя ISV следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14ff3-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="14ff3-149">Всегда используйте идентификатор ProgID, зависящий от приложения.</span><span class="sxs-lookup"><span data-stu-id="14ff3-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="14ff3-150">Применение соглашения о сопоставлении расширения имени файла с ProgID, предоставленным поставщиком программного обеспечения, позволяет избежать возможных конфликтов.</span><span class="sxs-lookup"><span data-stu-id="14ff3-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="14ff3-151">Однако, поскольку некоторые типы элементов не используют это сопоставление, существует потребность в уникальных именах поставщиков.</span><span class="sxs-lookup"><span data-stu-id="14ff3-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="14ff3-152">При добавлении команды к существующему идентификатору ProgID, который может уже зарегистрировать эту команду, необходимо сначала удалить раздел реестра для старой команды перед добавлением собственной команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="14ff3-153">Это необходимо сделать, чтобы избежать объединения сведений о командах из двух глаголов.</span><span class="sxs-lookup"><span data-stu-id="14ff3-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="14ff3-154">Несоблюдение этого действия приводит к непредсказуемому поведению.</span><span class="sxs-lookup"><span data-stu-id="14ff3-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="14ff3-155">Регистрация обработчика контекстного меню с динамической командой</span><span class="sxs-lookup"><span data-stu-id="14ff3-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="14ff3-156">Обработчики контекстного меню связаны либо с типом файла, либо с папкой.</span><span class="sxs-lookup"><span data-stu-id="14ff3-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="14ff3-157">Для типов файлов обработчик регистрируется в следующем подразделе.</span><span class="sxs-lookup"><span data-stu-id="14ff3-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="14ff3-158">Чтобы связать обработчик контекстного меню с типом файла или папкой, сначала создайте подраздел в подразделе **контекстменухандлерс** .</span><span class="sxs-lookup"><span data-stu-id="14ff3-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="14ff3-159">Назовите подраздел для обработчика и задайте в качестве значения по умолчанию для подраздела строковое значение GUID идентификатора класса обработчика (CLSID).</span><span class="sxs-lookup"><span data-stu-id="14ff3-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="14ff3-160">Затем, чтобы связать обработчик контекстного меню с разными типами папок, зарегистрируйте обработчик таким же образом, как для типа файлов, но в подразделе *фолдертипе* , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="14ff3-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="14ff3-161">Дополнительные сведения о типах папок, для которых можно зарегистрировать обработчики, см. в разделе [Регистрация обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="14ff3-162">Если с типом файла связано контекстное меню, то при двойном щелчке объекта обычно запускается команда по умолчанию, а метод [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) обработчика не вызывается.</span><span class="sxs-lookup"><span data-stu-id="14ff3-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="14ff3-163">Чтобы указать, что метод **IContextMenu:: куериконтекстмену** обработчика должен вызываться при двойном щелчке объекта, создайте подраздел в подразделе **CLSID** обработчика, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="14ff3-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="14ff3-164">При двойном щелчке объекта, связанного с обработчиком, вызывается [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) с флагом **КМФ \_ дефаултонли** , установленным в параметре *уфлагс* .</span><span class="sxs-lookup"><span data-stu-id="14ff3-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="14ff3-165">Обработчики контекстного меню должны задавать подраздел **майчанжедефаултмену** только в том случае, если им может потребоваться изменить команду по умолчанию в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="14ff3-166">Установка этого подраздела заставляет систему загружать DLL-библиотеку обработчика при двойном щелчке связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="14ff3-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="14ff3-167">Если обработчик не изменяет команду по умолчанию, этот подраздел задавать не следует, так как это приводит к тому, что система загружает библиотеку DLL без необходимости.</span><span class="sxs-lookup"><span data-stu-id="14ff3-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="14ff3-168">В следующем примере показаны записи реестра, которые включают обработчик контекстного меню для типа файла МИП.</span><span class="sxs-lookup"><span data-stu-id="14ff3-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="14ff3-169">Подраздел **CLSID** обработчика включает подраздел **майчанжедефаултмену** , гарантирующий, что обработчик вызывается, когда пользователь дважды щелкает связанный объект.</span><span class="sxs-lookup"><span data-stu-id="14ff3-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="14ff3-170">Реализация интерфейса IContextMenu</span><span class="sxs-lookup"><span data-stu-id="14ff3-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="14ff3-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) является самым мощным, но и самым сложным методом для реализации.</span><span class="sxs-lookup"><span data-stu-id="14ff3-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="14ff3-172">Настоятельно рекомендуется реализовать команду с помощью одного из статических методов глагола.</span><span class="sxs-lookup"><span data-stu-id="14ff3-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="14ff3-173">Дополнительные сведения см. в разделе [Выбор статической или динамической команды для контекстного меню](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="14ff3-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) содержит три метода: **жеткоммандстринг**, **инвокекомманд** и **куериконтекстмену**, которые подробно обсуждаются.</span><span class="sxs-lookup"><span data-stu-id="14ff3-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="14ff3-175">Метод IContextMenu:: Жеткоммандстринг</span><span class="sxs-lookup"><span data-stu-id="14ff3-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="14ff3-176">Метод [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) обработчика используется для возврата канонического имени для команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="14ff3-177">Этот метод является необязательным.</span><span class="sxs-lookup"><span data-stu-id="14ff3-177">This method is optional.</span></span> <span data-ttu-id="14ff3-178">В Windows XP и более ранних версиях Windows, когда в проводнике Windows есть строка состояния, этот метод используется для получения текста справки, который отображается в строке состояния для пункта меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="14ff3-179">Параметр *идкмд* содержит смещение идентификатора команды, которая была определена при вызове [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="14ff3-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="14ff3-180">При запросе строки справки для *уфлагс* будет задано значение **GC \_ хелптекств**.</span><span class="sxs-lookup"><span data-stu-id="14ff3-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="14ff3-181">Скопируйте строку справки в буфер *pszName* , приведя ее к **пвстр**.</span><span class="sxs-lookup"><span data-stu-id="14ff3-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="14ff3-182">Строка команды запрашивается путем установки *уфлагс* в **GC \_ вербв**.</span><span class="sxs-lookup"><span data-stu-id="14ff3-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="14ff3-183">Скопируйте соответствующую строку в *pszName*, точно так же, как и строку справки.</span><span class="sxs-lookup"><span data-stu-id="14ff3-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="14ff3-184">Флаги валидатев **GC \_** и **GC \_** не используются обработчиками контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="14ff3-185">В следующем примере показана простая реализация [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , которая соответствует примеру [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , приведенному в разделе [метод IContextMenu:: куериконтекстмену](#icontextmenuquerycontextmenu-method) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="14ff3-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="14ff3-186">Поскольку обработчик добавляет только один пункт меню, можно вернуть только один набор строк.</span><span class="sxs-lookup"><span data-stu-id="14ff3-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="14ff3-187">Метод проверяет, является ли *идкмд* допустимым, и, если это так, возвращает запрошенную строку.</span><span class="sxs-lookup"><span data-stu-id="14ff3-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="14ff3-188">Функция [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) используется для копирования запрашиваемой строки в *pszName* , чтобы гарантировать, что копируемая строка не превысит размер буфера, указанного в *кчнаме*.</span><span class="sxs-lookup"><span data-stu-id="14ff3-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="14ff3-189">В этом примере реализована поддержка только значений Юникода для *уфлагс*, поскольку только они использовались в проводнике Windows с момента выпуска Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="14ff3-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="14ff3-190">Метод IContextMenu:: Инвокекомманд</span><span class="sxs-lookup"><span data-stu-id="14ff3-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="14ff3-191">Этот метод вызывается, когда пользователь щелкает элемент меню, чтобы указать обработчику выполнить связанную команду.</span><span class="sxs-lookup"><span data-stu-id="14ff3-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="14ff3-192">Параметр *пиЦи* указывает на структуру, содержащую необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="14ff3-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="14ff3-193">Хотя *пиЦи* объявляется в шлобж. h как структура [**кминвокекоммандинфо**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , на практике он часто указывает на структуру [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="14ff3-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="14ff3-194">Эта структура является расширенной версией **кминвокекоммандинфо** и содержит несколько дополнительных членов, которые позволяют передавать строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="14ff3-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="14ff3-195">Проверьте член **кбсизе** объекта *пиЦи* , чтобы определить, какая структура была передана.</span><span class="sxs-lookup"><span data-stu-id="14ff3-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="14ff3-196">Если это структура [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) , а у члена **фмаск** установлен флаг **\_ \_ Юникода Mask** , приведите *пиЦи* к **кминвокекоммандинфоекс**.</span><span class="sxs-lookup"><span data-stu-id="14ff3-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="14ff3-197">Это позволяет приложению использовать сведения в Юникоде, содержащиеся в последних пяти элементах структуры.</span><span class="sxs-lookup"><span data-stu-id="14ff3-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="14ff3-198">Элемент **лпверб** или **лпвербв** структуры используется для задания выполняемой команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="14ff3-199">Команды идентифицируются одним из следующих двух способов.</span><span class="sxs-lookup"><span data-stu-id="14ff3-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="14ff3-200">В строке команд команды</span><span class="sxs-lookup"><span data-stu-id="14ff3-200">By the command's verb string</span></span>
-   <span data-ttu-id="14ff3-201">По смещению идентификатора команды</span><span class="sxs-lookup"><span data-stu-id="14ff3-201">By the command's identifier offset</span></span>

<span data-ttu-id="14ff3-202">Чтобы отличить эти два варианта, проверьте, что в регистре Юникода или **лпвербв** используется слово высокого порядка **ЛПВЕРБ** для регистра ANSI.</span><span class="sxs-lookup"><span data-stu-id="14ff3-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="14ff3-203">Если слово с высоким порядком не равно нулю, **лпверб** или **лпвербв** содержит строку команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="14ff3-204">Если слово с высоким порядковым значением равно нулю, то смещение команды находится в слове **лпверб** нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="14ff3-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="14ff3-205">В следующем примере показана простая реализация [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , которая соответствует примерам [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) и [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , заданным до и после этого раздела.</span><span class="sxs-lookup"><span data-stu-id="14ff3-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="14ff3-206">Сначала метод определяет, какая структура передается.</span><span class="sxs-lookup"><span data-stu-id="14ff3-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="14ff3-207">Затем он определяет, определена ли команда по смещению или ее команде.</span><span class="sxs-lookup"><span data-stu-id="14ff3-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="14ff3-208">Если **лпверб** или **лпвербв** содержит допустимую глагол или смещение, метод отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="14ff3-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="14ff3-209">Метод IContextMenu:: Куериконтекстмену</span><span class="sxs-lookup"><span data-stu-id="14ff3-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="14ff3-210">Оболочка вызывает [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , чтобы обработчик контекстного меню добавим в меню соответствующие элементы меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="14ff3-211">Он передает маркер **HMENU** в параметре *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="14ff3-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="14ff3-212">Для параметра *индексмену* задается индекс, используемый для первого добавляемого элемента меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="14ff3-213">Все элементы меню, добавленные обработчиком, должны иметь идентификаторы, попадающие в значения параметров *идкмдфирст* и *идкмдласт* .</span><span class="sxs-lookup"><span data-stu-id="14ff3-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="14ff3-214">Как правило, первый идентификатор команды имеет значение *идкмдфирст*, что увеличивается на единицу (1) для каждой дополнительной команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="14ff3-215">Такой подход позволяет избежать превышения *идкмдласт* и максимально увеличить количество доступных идентификаторов в случае, если оболочка вызывает более одного обработчика.</span><span class="sxs-lookup"><span data-stu-id="14ff3-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="14ff3-216">*Смещение команды* идентификатора элемента — это разница между идентификатором и значением в *идкмдфирст*.</span><span class="sxs-lookup"><span data-stu-id="14ff3-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="14ff3-217">Сохраните смещение каждого элемента, добавляемого обработчиком, в контекстное меню, так как оболочка может использовать его для обнаружения элемента, если впоследствии вызывает [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) или [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="14ff3-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="14ff3-218">Необходимо также назначить [команду](launch.md) каждой добавляемой команде.</span><span class="sxs-lookup"><span data-stu-id="14ff3-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="14ff3-219">Глагол — это строка, которую можно использовать вместо смещения для обнаружения команды при вызове [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="14ff3-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="14ff3-220">Он также используется такими функциями, как [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения команд контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="14ff3-221">Существует три флага, которые можно передать с помощью параметра *уфлагс* , относящегося к обработчикам контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="14ff3-222">Они описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="14ff3-222">They are described in the following table.</span></span>



| <span data-ttu-id="14ff3-223">Flag</span><span class="sxs-lookup"><span data-stu-id="14ff3-223">Flag</span></span>             | <span data-ttu-id="14ff3-224">Описание</span><span class="sxs-lookup"><span data-stu-id="14ff3-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ff3-225">КМФ \_ дефаултонли</span><span class="sxs-lookup"><span data-stu-id="14ff3-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="14ff3-226">Пользователь выбрал команду по умолчанию, обычно дважды щелкнув объект.</span><span class="sxs-lookup"><span data-stu-id="14ff3-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="14ff3-227">[**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) должен возвращать управление в оболочку без изменения меню.</span><span class="sxs-lookup"><span data-stu-id="14ff3-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="14ff3-228">КМФ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="14ff3-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="14ff3-229">Ни один элемент в меню не должен быть элементом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14ff3-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="14ff3-230">Метод должен добавить в меню свои команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="14ff3-231">КМФ, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="14ff3-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="14ff3-232">Контекстное меню будет отображаться в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="14ff3-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="14ff3-233">Метод должен добавить в меню свои команды.</span><span class="sxs-lookup"><span data-stu-id="14ff3-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="14ff3-234">Чтобы добавить пункты меню в список, используйте [**инсертмену**](/windows/win32/api/winuser/nf-winuser-insertmenua) или [**инсертменуитем**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) .</span><span class="sxs-lookup"><span data-stu-id="14ff3-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="14ff3-235">Затем возвращается значение **HRESULT** с уровнем серьезности " **\_ успешно**".</span><span class="sxs-lookup"><span data-stu-id="14ff3-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="14ff3-236">В качестве значения кода задайте смещение самого крупного идентификатора команды, который был назначен, плюс один (1).</span><span class="sxs-lookup"><span data-stu-id="14ff3-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="14ff3-237">Например, предположим, что *идкмдфирст* имеет значение 5, и в меню добавляются три элемента с идентификаторами команд 5, 7 и 8.</span><span class="sxs-lookup"><span data-stu-id="14ff3-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="14ff3-238">Возвращаемое значение должно быть `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="14ff3-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="14ff3-239">В следующем примере показана простая реализация [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , которая вставляет одну команду.</span><span class="sxs-lookup"><span data-stu-id="14ff3-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="14ff3-240">Смещение идентификатора для команды равно \_ отображению IDM, для которого задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="14ff3-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="14ff3-241">Переменные **m \_ псзверб** и **m \_ пвсзверб** являются частными переменными, которые используются для хранения связанной с ними независимой от языка строки в форматах ANSI и Unicode.</span><span class="sxs-lookup"><span data-stu-id="14ff3-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="14ff3-242">Сведения о других задачах реализации команд см. в разделе [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="14ff3-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14ff3-243">См. также</span><span class="sxs-lookup"><span data-stu-id="14ff3-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14ff3-244">Контекстное меню (контекст) и обработчики контекстного меню</span><span class="sxs-lookup"><span data-stu-id="14ff3-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="14ff3-245">Команды и сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="14ff3-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="14ff3-246">Выбор статической или динамической команды для контекстного меню</span><span class="sxs-lookup"><span data-stu-id="14ff3-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="14ff3-247">Рекомендации по работе с обработчиками контекстного меню и несколькими командами выбора</span><span class="sxs-lookup"><span data-stu-id="14ff3-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="14ff3-248">Создание обработчиков контекстного меню</span><span class="sxs-lookup"><span data-stu-id="14ff3-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="14ff3-249">Справочник по контекстному меню</span><span class="sxs-lookup"><span data-stu-id="14ff3-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 

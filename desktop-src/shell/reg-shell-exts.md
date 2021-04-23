---
description: Прежде чем оболочку сможет его использовать, необходимо зарегистрировать объект обработчика расширения оболочки. В этом разделе описывается, как зарегистрировать обработчик расширения оболочки.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Регистрация обработчиков расширений оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985761"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="a983e-104">Регистрация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="a983e-105">Прежде чем оболочку сможет его использовать, необходимо зарегистрировать объект обработчика расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="a983e-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="a983e-106">В этом разделе описывается, как зарегистрировать обработчик расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="a983e-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="a983e-107">Каждый раз при создании или изменении обработчика расширений оболочки важно уведомлять систему, что вы внесли изменения.</span><span class="sxs-lookup"><span data-stu-id="a983e-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="a983e-108">Для этого вызовите [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), указав событие **\_ ассокчанжед шкне** .</span><span class="sxs-lookup"><span data-stu-id="a983e-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="a983e-109">Если не вызвать **шчанженотифи**, изменение может быть не распознано, пока система не будет перезагружена.</span><span class="sxs-lookup"><span data-stu-id="a983e-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="a983e-110">Существуют некоторые дополнительные факторы, которые относятся к системам Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a983e-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="a983e-111">Дополнительные сведения см. в разделе [Регистрация обработчиков расширения оболочки в системах Windows 2000](#registering-shell-extension-handlers) .</span><span class="sxs-lookup"><span data-stu-id="a983e-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="a983e-112">Как и для всех COM-объектов, необходимо создать идентификатор GUID для обработчика с помощью такого средства, как Guidgen.exe, которое предоставляется вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="a983e-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a983e-113">Создайте подраздел в разделе **\_ классы hKey \_ root** \\ **CLSID** , имя которого является строковым форматом этого GUID.</span><span class="sxs-lookup"><span data-stu-id="a983e-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="a983e-114">Так как обработчики расширений оболочки являются внутрипроцессного серверами, необходимо также создать подраздел **InprocServer32** в этом подразделе GUID со значением (по умолчанию), равным пути к DLL-файлу обработчика.</span><span class="sxs-lookup"><span data-stu-id="a983e-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="a983e-115">Используйте модель потоков подразделений.</span><span class="sxs-lookup"><span data-stu-id="a983e-115">Use the apartment threading model.</span></span> <span data-ttu-id="a983e-116">Пример показан далее:</span><span class="sxs-lookup"><span data-stu-id="a983e-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="a983e-117">Каждый раз, когда оболочка принимает действие, которое может задействовать обработчик расширения оболочки, он проверяет соответствующий подраздел реестра.</span><span class="sxs-lookup"><span data-stu-id="a983e-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="a983e-118">Подключ, по которому обработчик расширений регистрирует элементы управления при его вызове.</span><span class="sxs-lookup"><span data-stu-id="a983e-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="a983e-119">Например, при отображении оболочкой контекстного меню для элемента [типа файла](fa-file-types.md)обычно вызывается обработчик контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="a983e-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="a983e-120">В этом случае обработчик должен быть зарегистрирован в подразделе **ProgID** типа файла.</span><span class="sxs-lookup"><span data-stu-id="a983e-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="a983e-121">В этом разделе обсуждаются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="a983e-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="a983e-122">Имена обработчиков</span><span class="sxs-lookup"><span data-stu-id="a983e-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="a983e-123">Предопределенные объекты оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="a983e-124">Пример регистрации обработчика расширений</span><span class="sxs-lookup"><span data-stu-id="a983e-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="a983e-125">Регистрация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="a983e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a983e-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="a983e-127">Имена обработчиков</span><span class="sxs-lookup"><span data-stu-id="a983e-127">Handler Names</span></span>

<span data-ttu-id="a983e-128">Чтобы включить обработчик расширений оболочки, создайте подраздел с именем подраздела обработчика (см. ниже) в подразделе **шеллекс** (для типов файлов) **или в имени** типа объекта оболочки (для [предопределенных \_ \_ объектов оболочки](handlers.md)).</span><span class="sxs-lookup"><span data-stu-id="a983e-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="a983e-129">Например, если вы хотите зарегистрировать обработчик расширения контекстного меню для MyProgram. 1, начните с создания следующего подраздела:</span><span class="sxs-lookup"><span data-stu-id="a983e-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="a983e-130">Для следующих обработчиков создайте подраздел под подразделом "имя подраздела обработчика" с именем в виде строкового версии идентификатора класса (CLSID) расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="a983e-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="a983e-131">Несколько расширений можно зарегистрировать в имени подраздела обработчика, создав несколько подразделов.</span><span class="sxs-lookup"><span data-stu-id="a983e-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="a983e-132">Обработчик</span><span class="sxs-lookup"><span data-stu-id="a983e-132">Handler</span></span>                 | <span data-ttu-id="a983e-133">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="a983e-133">Interface</span></span>          | <span data-ttu-id="a983e-134">Имя подраздела обработчика</span><span class="sxs-lookup"><span data-stu-id="a983e-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="a983e-135">Обработчик поставщика столбцов</span><span class="sxs-lookup"><span data-stu-id="a983e-135">Column provider handler</span></span> | <span data-ttu-id="a983e-136">иколумнпровидер</span><span class="sxs-lookup"><span data-stu-id="a983e-136">IColumnProvider</span></span>    | <span data-ttu-id="a983e-137">**колумнхандлерс**</span><span class="sxs-lookup"><span data-stu-id="a983e-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="a983e-138">Обработчик контекстного меню</span><span class="sxs-lookup"><span data-stu-id="a983e-138">Shortcut menu handler</span></span>   | <span data-ttu-id="a983e-139">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a983e-139">IContextMenu</span></span>       | <span data-ttu-id="a983e-140">**контекстменухандлерс**</span><span class="sxs-lookup"><span data-stu-id="a983e-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="a983e-141">Обработчик копихук</span><span class="sxs-lookup"><span data-stu-id="a983e-141">Copyhook handler</span></span>        | <span data-ttu-id="a983e-142">икопихук</span><span class="sxs-lookup"><span data-stu-id="a983e-142">ICopyHook</span></span>          | <span data-ttu-id="a983e-143">**копихукхандлерс**</span><span class="sxs-lookup"><span data-stu-id="a983e-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="a983e-144">Обработчик действия перетаскивания</span><span class="sxs-lookup"><span data-stu-id="a983e-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="a983e-145">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="a983e-145">IContextMenu</span></span>       | <span data-ttu-id="a983e-146">**драгдрофандлерс**</span><span class="sxs-lookup"><span data-stu-id="a983e-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="a983e-147">Обработчик страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a983e-147">Property sheet handler</span></span>  | <span data-ttu-id="a983e-148">ишеллпропшитекст</span><span class="sxs-lookup"><span data-stu-id="a983e-148">IShellPropSheetExt</span></span> | <span data-ttu-id="a983e-149">**пропертишисандлерс**</span><span class="sxs-lookup"><span data-stu-id="a983e-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="a983e-150">Для следующих обработчиков значение по умолчанию ключа "имя подраздела обработчика" является строковой версией CLSID расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="a983e-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="a983e-151">Для этих обработчиков можно зарегистрировать только одно расширение.</span><span class="sxs-lookup"><span data-stu-id="a983e-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="a983e-152">Обработчик</span><span class="sxs-lookup"><span data-stu-id="a983e-152">Handler</span></span>                 | <span data-ttu-id="a983e-153">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="a983e-153">Interface</span></span>            | <span data-ttu-id="a983e-154">Имя подраздела обработчика</span><span class="sxs-lookup"><span data-stu-id="a983e-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="a983e-155">Обработчик данных</span><span class="sxs-lookup"><span data-stu-id="a983e-155">Data handler</span></span>            | <span data-ttu-id="a983e-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="a983e-156">IDataObject</span></span>          | <span data-ttu-id="a983e-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="a983e-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="a983e-158">Удалить обработчик</span><span class="sxs-lookup"><span data-stu-id="a983e-158">Drop handler</span></span>            | <span data-ttu-id="a983e-159">Интерфейс IDropTarget</span><span class="sxs-lookup"><span data-stu-id="a983e-159">IDropTarget</span></span>          | <span data-ttu-id="a983e-160">**дрофандлер**</span><span class="sxs-lookup"><span data-stu-id="a983e-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="a983e-161">Обработчик значков</span><span class="sxs-lookup"><span data-stu-id="a983e-161">Icon handler</span></span>            | <span data-ttu-id="a983e-162">Иекстрактикона/W</span><span class="sxs-lookup"><span data-stu-id="a983e-162">IExtractIconA/W</span></span>      | <span data-ttu-id="a983e-163">**иконхандлер**</span><span class="sxs-lookup"><span data-stu-id="a983e-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="a983e-164">Обработчик изображений эскиза</span><span class="sxs-lookup"><span data-stu-id="a983e-164">Thumbnail image handler</span></span> | <span data-ttu-id="a983e-165">исумбнаилпровидер</span><span class="sxs-lookup"><span data-stu-id="a983e-165">IThumbnailProvider</span></span>   | <span data-ttu-id="a983e-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="a983e-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="a983e-167">Обработчик подсказок</span><span class="sxs-lookup"><span data-stu-id="a983e-167">Infotip handler</span></span>         | <span data-ttu-id="a983e-168">икуеринфо</span><span class="sxs-lookup"><span data-stu-id="a983e-168">IQueryInfo</span></span>           | <span data-ttu-id="a983e-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="a983e-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="a983e-170">Ссылка на оболочку (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a983e-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="a983e-171">ишелллинка</span><span class="sxs-lookup"><span data-stu-id="a983e-171">IShellLinkA</span></span>          | <span data-ttu-id="a983e-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="a983e-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="a983e-173">Ссылка на оболочку (Юникод)</span><span class="sxs-lookup"><span data-stu-id="a983e-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="a983e-174">ишелллинкв</span><span class="sxs-lookup"><span data-stu-id="a983e-174">IShellLinkW</span></span>          | <span data-ttu-id="a983e-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="a983e-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="a983e-176">Структурированное хранилище</span><span class="sxs-lookup"><span data-stu-id="a983e-176">Structured storage</span></span>      | <span data-ttu-id="a983e-177">Метод IStorage</span><span class="sxs-lookup"><span data-stu-id="a983e-177">IStorage</span></span>             | <span data-ttu-id="a983e-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="a983e-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="a983e-179">Метаданные</span><span class="sxs-lookup"><span data-stu-id="a983e-179">Metadata</span></span>                | <span data-ttu-id="a983e-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="a983e-180">IPropertySetStorage</span></span>  | <span data-ttu-id="a983e-181">**пропертихандлер**</span><span class="sxs-lookup"><span data-stu-id="a983e-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="a983e-182">Закрепить в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="a983e-182">Pin to Start Menu</span></span>       | <span data-ttu-id="a983e-183">истартменупиннедлист</span><span class="sxs-lookup"><span data-stu-id="a983e-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="a983e-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="a983e-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="a983e-185">Закрепление на панели задач</span><span class="sxs-lookup"><span data-stu-id="a983e-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="a983e-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="a983e-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="a983e-187">Подразделы, указанные для добавления **закрепления в меню "Пуск** " и " **закрепить на панели задач** " в контекстном меню элемента, необходимы только для типов файлов, включающих запись " [ярлык](./links.md) ".</span><span class="sxs-lookup"><span data-stu-id="a983e-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="a983e-188">Предопределенные объекты оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-188">Predefined Shell Objects</span></span>

<span data-ttu-id="a983e-189">Оболочка определяет дополнительные объекты в **\_ \_ корне классов hKey** , которые могут быть расширены так же, как и типы файлов.</span><span class="sxs-lookup"><span data-stu-id="a983e-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="a983e-190">Например, чтобы добавить обработчик страницы свойств для всех файлов, можно выполнить регистрацию в подразделе **пропертишисандлерс** .</span><span class="sxs-lookup"><span data-stu-id="a983e-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="a983e-191">В следующей таблице приведены различные подразделы **\_ \_ корня классов hKey** , в которых можно регистрировать обработчики расширений.</span><span class="sxs-lookup"><span data-stu-id="a983e-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="a983e-192">Обратите внимание, что многие обработчики расширений не могут быть зарегистрированы во всех перечисленных подразделах.</span><span class="sxs-lookup"><span data-stu-id="a983e-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="a983e-193">Дополнительные сведения см. в документации по конкретному обработчику.</span><span class="sxs-lookup"><span data-stu-id="a983e-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="a983e-194">Подраздел</span><span class="sxs-lookup"><span data-stu-id="a983e-194">Subkey</span></span>                    | <span data-ttu-id="a983e-195">Описание</span><span class="sxs-lookup"><span data-stu-id="a983e-195">Description</span></span>                                                          | <span data-ttu-id="a983e-196">Возможные обработчики</span><span class="sxs-lookup"><span data-stu-id="a983e-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="a983e-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="a983e-197">\**\** _</span></span>                    | <span data-ttu-id="a983e-198">Все файлы</span><span class="sxs-lookup"><span data-stu-id="a983e-198">All files</span></span>                                                            | <span data-ttu-id="a983e-199">Контекстное меню, страница свойств, команды (см. ниже)</span><span class="sxs-lookup"><span data-stu-id="a983e-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="a983e-200">_ *Аллфилесистемобжектс*\*</span><span class="sxs-lookup"><span data-stu-id="a983e-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="a983e-201">Все файлы и папки с файлами</span><span class="sxs-lookup"><span data-stu-id="a983e-201">All files and file folders</span></span>                                           | <span data-ttu-id="a983e-202">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-203">**Папка**</span><span class="sxs-lookup"><span data-stu-id="a983e-203">**Folder**</span></span>                | <span data-ttu-id="a983e-204">Все папки</span><span class="sxs-lookup"><span data-stu-id="a983e-204">All folders</span></span>                                                          | <span data-ttu-id="a983e-205">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-206">**Каталог**</span><span class="sxs-lookup"><span data-stu-id="a983e-206">**Directory**</span></span>             | <span data-ttu-id="a983e-207">Папки с файлами</span><span class="sxs-lookup"><span data-stu-id="a983e-207">File folders</span></span>                                                         | <span data-ttu-id="a983e-208">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-209">**\\Фон каталога**</span><span class="sxs-lookup"><span data-stu-id="a983e-209">**Directory\\Background**</span></span> | <span data-ttu-id="a983e-210">Фон папки файлов</span><span class="sxs-lookup"><span data-stu-id="a983e-210">File folder background</span></span>                                               | <span data-ttu-id="a983e-211">Только контекстное меню</span><span class="sxs-lookup"><span data-stu-id="a983e-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="a983e-212">**десктопбаккграунд**</span><span class="sxs-lookup"><span data-stu-id="a983e-212">**DesktopBackground**</span></span>     | <span data-ttu-id="a983e-213">Фон рабочего стола (Windows 7 и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="a983e-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="a983e-214">Контекстное меню, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="a983e-215">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="a983e-215">**Drive**</span></span>                 | <span data-ttu-id="a983e-216">Все диски в MyComputer, например "C: \\ "</span><span class="sxs-lookup"><span data-stu-id="a983e-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="a983e-217">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-218">**Network**</span><span class="sxs-lookup"><span data-stu-id="a983e-218">**Network**</span></span>               | <span data-ttu-id="a983e-219">Вся сеть (в разделе Мое сетевое окружение)</span><span class="sxs-lookup"><span data-stu-id="a983e-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="a983e-220">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-221">**\\Тип сети\\\#**</span><span class="sxs-lookup"><span data-stu-id="a983e-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="a983e-222">Все объекты типа \# (см. ниже)</span><span class="sxs-lookup"><span data-stu-id="a983e-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="a983e-223">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-224">**нетшаре**</span><span class="sxs-lookup"><span data-stu-id="a983e-224">**NetShare**</span></span>              | <span data-ttu-id="a983e-225">Все общие сетевые папки</span><span class="sxs-lookup"><span data-stu-id="a983e-225">All network shares</span></span>                                                   | <span data-ttu-id="a983e-226">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-227">**нетсервер**</span><span class="sxs-lookup"><span data-stu-id="a983e-227">**NetServer**</span></span>             | <span data-ttu-id="a983e-228">Все сетевые серверы</span><span class="sxs-lookup"><span data-stu-id="a983e-228">All network servers</span></span>                                                  | <span data-ttu-id="a983e-229">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-230">*\_имя поставщика \_ сети*</span><span class="sxs-lookup"><span data-stu-id="a983e-230">*network\_provider\_name*</span></span> | <span data-ttu-id="a983e-231">Все объекты, предоставляемые поставщиком сетевых услуг "*\_ \_ имя поставщика* сети"</span><span class="sxs-lookup"><span data-stu-id="a983e-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="a983e-232">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="a983e-233">**принтеры;**</span><span class="sxs-lookup"><span data-stu-id="a983e-233">**Printers**</span></span>              | <span data-ttu-id="a983e-234">Все принтеры</span><span class="sxs-lookup"><span data-stu-id="a983e-234">All printers</span></span>                                                         | <span data-ttu-id="a983e-235">Контекстное меню, страница свойств</span><span class="sxs-lookup"><span data-stu-id="a983e-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="a983e-236">**аудиокд**</span><span class="sxs-lookup"><span data-stu-id="a983e-236">**AudioCD**</span></span>               | <span data-ttu-id="a983e-237">Звуковой компакт-диск в дисководе компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="a983e-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="a983e-238">Только глаголы</span><span class="sxs-lookup"><span data-stu-id="a983e-238">Verbs only</span></span>                                       |
| <span data-ttu-id="a983e-239">**ОПТИЧЕСКИ**</span><span class="sxs-lookup"><span data-stu-id="a983e-239">**DVD**</span></span>                   | <span data-ttu-id="a983e-240">DVD-дисковод (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="a983e-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="a983e-241">Контекстное меню, страница свойств, команды</span><span class="sxs-lookup"><span data-stu-id="a983e-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="a983e-242">Примечания</span><span class="sxs-lookup"><span data-stu-id="a983e-242">Notes</span></span>

-   <span data-ttu-id="a983e-243">Доступ к контекстному меню фонового доступа к папке осуществляется путем щелчка правой кнопкой мыши в папке файла, но не для содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="a983e-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="a983e-244">"Глаголы" — это специальные команды, зарегистрированные в команде оболочки **\_ \_ корневого** \\ *подраздела* для классов hKey \\  \\ .</span><span class="sxs-lookup"><span data-stu-id="a983e-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="a983e-245">Для  \\ **типа** сети \\ **\#** " \# " — это код типа поставщика сети в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="a983e-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="a983e-246">Код типа поставщика сети — это старшее слово типа сети.</span><span class="sxs-lookup"><span data-stu-id="a983e-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="a983e-247">Список сетевых типов указан в файле заголовка Виннетвк. h ( \_ значения вннк NET \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="a983e-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="a983e-248">Например, вннк \_ net " \_ 0x00330000", поэтому соответствующий подраздел типа будет содержать **\_ классы hKey \_ root** \\ **Network** \\ **Type** \\ **51**.</span><span class="sxs-lookup"><span data-stu-id="a983e-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="a983e-249">"*\_ \_ имя поставщика сети*" — это имя поставщика сети, указанное в [**внетжетпровидернаме**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), а пробелы преобразуются в символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a983e-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="a983e-250">Например, если установлен поставщик сетевых сетей Microsoft, его имя поставщика — «Microsoft Windows Network», а соответствующее *\_ \_ имя поставщика сети* — **Microsoft \_ Windows \_ Network**.</span><span class="sxs-lookup"><span data-stu-id="a983e-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="a983e-251">Пример регистрации обработчика расширений</span><span class="sxs-lookup"><span data-stu-id="a983e-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="a983e-252">Чтобы включить определенный обработчик, создайте подраздел в подразделе типа обработчика расширений с именем обработчика.</span><span class="sxs-lookup"><span data-stu-id="a983e-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="a983e-253">Оболочка не использует имя обработчика, но должно отличаться от всех других имен в подразделе этого типа.</span><span class="sxs-lookup"><span data-stu-id="a983e-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="a983e-254">Задайте значение по умолчанию для подраздела Name в виде строки идентификатора GUID обработчика.</span><span class="sxs-lookup"><span data-stu-id="a983e-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="a983e-255">В следующем примере показаны записи реестра, которые позволяют использовать контекстное меню и обработчики расширений страниц свойств с использованием типа файла example. МИП.</span><span class="sxs-lookup"><span data-stu-id="a983e-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="a983e-256">Регистрация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="a983e-257">Процедура регистрации, описанная в этом разделе, должна соблюдаться для всех систем Windows.</span><span class="sxs-lookup"><span data-stu-id="a983e-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="a983e-258">Однако в более поздних системах может потребоваться дополнительный шаг.</span><span class="sxs-lookup"><span data-stu-id="a983e-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="a983e-259">Поскольку эти более поздние версии Windows предназначены для использования в управляемой среде, доступ к реестру может быть ограничен административно, что требует немного другого подхода к установке, чем описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="a983e-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="a983e-260">Обычно программы установки не записываются непосредственно в реестр.</span><span class="sxs-lookup"><span data-stu-id="a983e-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="a983e-261">Вместо этого следует выполнить установку с помощью пакетов установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="a983e-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="a983e-262">Эти средства гарантируют, что программное обеспечение работает правильно и предоставляет доступ к таким возможностям, как регистрация на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="a983e-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="a983e-263">Обработчики расширений оболочки выполняются в процессе оболочки.</span><span class="sxs-lookup"><span data-stu-id="a983e-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="a983e-264">Поскольку это системный процесс, администратор системы может ограничить обработчики расширений оболочки до тех, которые включены в список утвержденных, задав для ключа **обозревателя** значение 1, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="a983e-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="a983e-265">Чтобы поместить обработчик расширения оболочки в список утвержденных, создайте значение **reg \_ SZ** , имя которого является СТРОКОВЫМ форматом идентификатора GUID обработчика в **утвержденном** подразделе.</span><span class="sxs-lookup"><span data-stu-id="a983e-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="a983e-266">Например, в следующем примере обработчики *микомманд* и *мипропшит* добавляются в список утвержденных.</span><span class="sxs-lookup"><span data-stu-id="a983e-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="a983e-267">Оболочка не использует значение, присвоенное идентификатору GUID, но оно должно быть настроено для упрощения проверки реестра.</span><span class="sxs-lookup"><span data-stu-id="a983e-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="a983e-268">Приложение установки может добавлять значения в **подразделы только в том случае** , если пользователь, устанавливающий приложение, имеет достаточные привилегии.</span><span class="sxs-lookup"><span data-stu-id="a983e-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="a983e-269">Если попытка добавления обработчика расширения завершается неудачно, необходимо сообщить пользователю, что для полной установки приложения требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="a983e-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="a983e-270">Если обработчик важен для приложения, следует завершить установку и уведомить пользователя о необходимости обратиться к администратору.</span><span class="sxs-lookup"><span data-stu-id="a983e-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a983e-271">См. также</span><span class="sxs-lookup"><span data-stu-id="a983e-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a983e-272">Инициализация обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="a983e-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 

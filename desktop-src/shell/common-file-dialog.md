---
description: Начиная с Windows Vista, диалоговое окно общих элементов заменяет более старое общее диалоговое окно файла при использовании для открытия или сохранения файла.
title: Диалоговое окно общих элементов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342845"
---
# <a name="common-item-dialog"></a><span data-ttu-id="a7bd7-103">Диалоговое окно общих элементов</span><span class="sxs-lookup"><span data-stu-id="a7bd7-103">Common Item Dialog</span></span>

<span data-ttu-id="a7bd7-104">Начиная с Windows Vista, диалоговое окно общих элементов заменяет более старое общее диалоговое окно файла при использовании для открытия или сохранения файла.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="a7bd7-105">Диалоговое окно Общие элементы используется в двух вариантах: диалоговое окно **Открыть** и диалоговое окно **сохранения** .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="a7bd7-106">Эти два диалоговых окна имеют большую часть их функциональных возможностей, но каждый из них имеет собственные уникальные методы.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="a7bd7-107">Хотя эта новая версия называется диалоговым окном общих элементов, она по-своему по-своему часто называется общим диалоговым окном файла.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="a7bd7-108">Если вы не работаете исключительно с более старой версией Windows, следует предположить, что любое упоминание общего диалогового окна с файлом относится к этому диалоговому окну общих элементов.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="a7bd7-109">Здесь обсуждаются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="a7bd7-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="a7bd7-110">Ифиледиалог, Ифилеопендиалог и Ифилесаведиалог</span><span class="sxs-lookup"><span data-stu-id="a7bd7-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="a7bd7-111">Пример использования</span><span class="sxs-lookup"><span data-stu-id="a7bd7-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="a7bd7-112">Прослушивание событий из диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="a7bd7-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="a7bd7-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="a7bd7-114">Оншаревиолатион и Оноверврите</span><span class="sxs-lookup"><span data-stu-id="a7bd7-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="a7bd7-115">Настройка диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="a7bd7-116">Добавление параметров к кнопке «ОК»</span><span class="sxs-lookup"><span data-stu-id="a7bd7-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="a7bd7-117">Реагирование на события в добавленных элементах управления</span><span class="sxs-lookup"><span data-stu-id="a7bd7-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="a7bd7-118">Полные примеры</span><span class="sxs-lookup"><span data-stu-id="a7bd7-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="a7bd7-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a7bd7-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="a7bd7-120">Ифиледиалог, Ифилеопендиалог и Ифилесаведиалог</span><span class="sxs-lookup"><span data-stu-id="a7bd7-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="a7bd7-121">В Windows Vista реализованы диалоговые окна **открытия** и **сохранения** : CLSID \_ филеопендиалог и CLSID \_ филесаведиалог.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="a7bd7-122">Эти диалоговые окна показаны здесь.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-122">Those dialog boxes are shown here.</span></span>

![снимок экрана диалогового окна "Открыть"](images/cid/openfiledialog.png)

![снимок экрана — диалоговое окно "Сохранить как"](images/cid/savefiledialog.png)

<span data-ttu-id="a7bd7-125">[**Ифилеопендиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) и [**ифилесаведиалог**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) наследуют от [**ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) и используют большую часть их функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="a7bd7-126">Кроме того, диалоговое окно **Открыть** поддерживает **ифилеопендиалог**, а диалоговое окно **сохранения** поддерживает **ифилесаведиалог**.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="a7bd7-127">Реализация общего элемента диалогового окна в Windows Vista предоставляет несколько преимуществ по сравнению с реализацией, реализованной в предыдущих версиях:</span><span class="sxs-lookup"><span data-stu-id="a7bd7-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="a7bd7-128">Поддерживает непосредственное использование пространства имен оболочки через [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) вместо использования путей файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="a7bd7-129">Включает простую настройку диалогового окна, например задание метки на кнопке « **ОК** » без необходимости выполнения процедуры обработчика.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="a7bd7-130">Поддерживает более обширную настройку диалогового окна за счет добавления набора элементов управления, управляемых данными, которые работают без шаблона диалогового окна Win32.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="a7bd7-131">Эта схема настройки освобождает вызывающий процесс от макета пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="a7bd7-132">Поскольку любые изменения в разработке диалогового окна продолжают использовать эту модель данных, реализация диалогового окна не привязана к конкретной текущей версии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="a7bd7-133">Поддерживает уведомление вызывающего объекта о событиях в диалоговом окне, например изменение выбора или изменение типа файла.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="a7bd7-134">Также позволяет вызывающему процессу подключать определенные события в диалоговом окне, например синтаксический анализ.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="a7bd7-135">В появились новые возможности диалогового окна, такие как добавление на панель **мест** определенных вызывающих объектов.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="a7bd7-136">В диалоговом окне **сохранения** разработчики могут воспользоваться новыми функциями метаданных оболочки Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="a7bd7-137">Кроме того, разработчики могут выбрать реализацию следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="a7bd7-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="a7bd7-138">[**Ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) для получения уведомлений о событиях в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="a7bd7-139">[**Ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , чтобы добавить элементы управления в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="a7bd7-140">[**Ифиледиалогконтролевентс**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) , чтобы получать уведомления о событиях в этих добавленных элементах управления.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="a7bd7-141">Диалоговое окно **открытия** или **сохранения** возвращает объект [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) или [**ишеллитемаррай**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) в вызывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="a7bd7-142">Затем вызывающий может использовать отдельный объект **интерфейса IShellItem** для получения пути к файловой системе или для открытия потока на элементе для чтения или записи данных.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="a7bd7-143">Флаги и параметры, доступные для новых методов диалогового окна, очень похожи на старые флаги **ОФН** , обнаруженные в структуре [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) и используемые в [**GetOpenFilename**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) и [**жетсавефиленаме**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="a7bd7-144">Многие из них идентичны, за исключением того, что они начинаются с префикса Фос.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="a7bd7-145">Полный список можно найти в разделах [**ифиледиалог::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) Ифиледиалог и [**:: сетоптионс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="a7bd7-146">Диалоговые окна **открытия** и **сохранения** создаются по умолчанию с самыми распространенными флагами.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="a7bd7-147">Для диалогового окна **Открыть** это (Фос \_ пасмустексист \| Фос \_ выполнить операцию filemustexist \| Фос \_ Ночанжедир) и для диалогового окна **сохранить** это (Фос овервритепромпт Фос \_ \| \_ нореадонлиретурн \| Фос пасмустексист FOS \_ \| \_ NOCHANGEDIR).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="a7bd7-148">[**Ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) и его дочерние интерфейсы наследуют от и расширяют [**имодалвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="a7bd7-149">Параметр [**Показывать**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) принимает в качестве единственного параметра маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="a7bd7-150">Если функция **Показывать** успешно возвращает значение, имеется допустимый результат.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="a7bd7-151">Если он возвращает значение `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , это означает, что пользователь отменил диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="a7bd7-152">Он также может вернуть другой код ошибки, например **E \_ OUTOFMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="a7bd7-153">Пример использования</span><span class="sxs-lookup"><span data-stu-id="a7bd7-153">Sample Usage</span></span>

<span data-ttu-id="a7bd7-154">В следующих разделах показан пример кода для различных задач диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="a7bd7-155">Базовое использование</span><span class="sxs-lookup"><span data-stu-id="a7bd7-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="a7bd7-156">Ограничение результатов для элементов файловой системы</span><span class="sxs-lookup"><span data-stu-id="a7bd7-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="a7bd7-157">Указание типов файлов для диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="a7bd7-158">Управление папкой по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7bd7-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="a7bd7-159">Добавление элементов на панель мест</span><span class="sxs-lookup"><span data-stu-id="a7bd7-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="a7bd7-160">Сохраняемость состояния</span><span class="sxs-lookup"><span data-stu-id="a7bd7-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="a7bd7-161">Возможности многовыборки</span><span class="sxs-lookup"><span data-stu-id="a7bd7-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="a7bd7-162">Большинство примеров кода можно найти в Windows SDK [общем файле](samples-commonfiledialog.md).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="a7bd7-163">Основное использование</span><span class="sxs-lookup"><span data-stu-id="a7bd7-163">Basic Usage</span></span>

<span data-ttu-id="a7bd7-164">В следующем примере показано, как запустить **открытое** диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="a7bd7-165">В этом примере он ограничен документами Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="a7bd7-166">Несколько примеров в этом разделе используют `CDialogEventHandler_CreateInstance` вспомогательную функцию для создания экземпляра реализации [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="a7bd7-167">Чтобы использовать эту функцию в собственном коде, скопируйте исходный код `CDialogEventHandler_CreateInstance` функции из [общего файлового диалога](samples-commonfiledialog.md), из которого берутся все примеры в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="a7bd7-168">Ограничение результатов для элементов файловой системы</span><span class="sxs-lookup"><span data-stu-id="a7bd7-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="a7bd7-169">В следующем примере, взятом из выше, показано, как ограничить результаты для элементов файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="a7bd7-170">Обратите внимание, что [**ифиледиалог:: сетоптионс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) добавляет новый флаг к значению, полученному с помощью [**ифиледиалог::-Options**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="a7bd7-171">Рекомендуем использовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="a7bd7-172">Указание типов файлов для диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="a7bd7-173">Чтобы задать определенные типы файлов, которые диалоговое окно может обработано, используйте метод [**ифиледиалог:: сетфилетипес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="a7bd7-174">Этот метод принимает массив структур [**комдлг \_ филтерспек**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , каждый из которых представляет тип файла.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="a7bd7-175">Механизм расширения по умолчанию в диалоговом окне не изменился с [**GetOpenFilename**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) и [**жетсавефиленаме**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="a7bd7-176">Расширение имени файла, добавляемое к тексту, которое пользователь вводит в поле ввода имени файла, инициализируется при открытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="a7bd7-177">Он должен соответствовать типу файла по умолчанию (который был выбран при открытии диалогового окна).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="a7bd7-178">Если тип файла по умолчанию — " \* . \* " (все файлы) файл может быть расширением по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="a7bd7-179">Если пользователь выбирает другой тип файла, расширение автоматически обновляет первое расширение имени файла, связанное с этим типом файлов.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="a7bd7-180">Если пользователь выбирает " \* . \* " (все файлы), расширение возвращается к исходному значению.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="a7bd7-181">В следующем примере показано, как это было сделано ранее.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="a7bd7-182">Управление папкой по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7bd7-182">Controlling the Default Folder</span></span>

<span data-ttu-id="a7bd7-183">Почти любую папку в пространстве имен Shell можно использовать в качестве папки по умолчанию для диалогового окна (папки, представленной при открытии или сохранении файла пользователем).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="a7bd7-184">Вызовите метод [**ифиледиалог:: сетдефаултфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) перед вызовом метода [**демонстрация**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="a7bd7-185">Папка по умолчанию — это папка, в которой диалоговое окно запускается при первом его открытии пользователем из приложения.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="a7bd7-186">После этого диалоговое окно откроется в последней папке, открытой пользователем, или в последней папке, используемой для сохранения элемента.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="a7bd7-187">Дополнительные сведения см. в разделе [Сохранение состояния](#state-persistence) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="a7bd7-188">Можно заставить диалоговое окно всегда отображать ту же папку при открытии, вне зависимости от предыдущего действия пользователя, вызывая [**ифиледиалог:: сетфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="a7bd7-189">Однако делать это не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="a7bd7-190">Если вызвать **сетфолдер** перед отображением диалогового окна, то Последнее расположение, которое пользователь сохранил или открыл из, не отображается.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="a7bd7-191">Если для этого поведения нет особой причины, это не является хорошим или ожидаемым пользовательским интерфейсом, и его следует избегать.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="a7bd7-192">В большинстве случаев метод [**ифиледиалог:: сетдефаултфолдер**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) является лучшим методом.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="a7bd7-193">При первом сохранении документа в диалоговом окне **сохранения** необходимо следовать тем же рекомендациям, что и при определении исходной папки, как это делалось в диалоговом окне **Открыть** .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="a7bd7-194">Если пользователь редактирует ранее существующий документ, откройте диалоговое окно в папке, в которой хранится этот документ, и заполните поле ввода именем этого документа.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="a7bd7-195">Вызовите [**ифилесаведиалог:: сетсавеаситем**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) с текущим элементом до вызова метода [**демонстрации**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="a7bd7-196">Добавление элементов на панель мест</span><span class="sxs-lookup"><span data-stu-id="a7bd7-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="a7bd7-197">В следующем примере показано добавление элементов на панель **мест** .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="a7bd7-198">Сохраняемость состояния</span><span class="sxs-lookup"><span data-stu-id="a7bd7-198">State Persistence</span></span>

<span data-ttu-id="a7bd7-199">До Windows Vista состояние, например Последнее посещение папки, было сохранено отдельно для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="a7bd7-200">Однако эта информация использовалась независимо от конкретного действия.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="a7bd7-201">Например, приложение для редактирования видео будет представлять ту же папку в диалоговом окне « **рендеринг как** », что и в диалоговом окне « **Импорт носителя** ».</span><span class="sxs-lookup"><span data-stu-id="a7bd7-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="a7bd7-202">В Windows Vista можно использовать более конкретные идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="a7bd7-203">Чтобы назначить **идентификатор GUID** для диалогового окна, вызовите метод [**Ифиледиалог:: сетклиентгуид**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="a7bd7-204">Возможности многовыборки</span><span class="sxs-lookup"><span data-stu-id="a7bd7-204">Multiselect Capabilities</span></span>

<span data-ttu-id="a7bd7-205">Функциональные возможности, доступные в диалоговом окне **Открыть** , можно получить с [**помощью метода,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="a7bd7-206">Прослушивание событий из диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="a7bd7-207">Вызывающий процесс может зарегистрировать интерфейс [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) в диалоговом окне с помощью методов [**Ифиледиалог:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) и [**ифиледиалог:: unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) , как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="a7bd7-208">Это взято из примера [использования Basic](#basic-usage) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="a7bd7-209">Основная часть обработки диалогового окна будет помещена здесь.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="a7bd7-210">Вызывающий процесс может использовать события для уведомления о том, что пользователь изменяет папку, тип файла или выделенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="a7bd7-211">Эти события особенно полезны, когда вызывающий процесс добавил элементы управления в диалоговое окно (см. раздел [Настройка диалогового окна](#customizing-the-dialog)) и должен изменить состояние этих элементов управления в реакцию на эти события.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="a7bd7-212">Полезным во всех случаях является способность вызывающего процесса предоставлять пользовательский код для решения таких ситуаций, как нарушения совместного доступа, перезапись файлов или определение допустимости файла перед закрытием диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="a7bd7-213">Некоторые из этих случаев описаны в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="a7bd7-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="a7bd7-214">OnFileOk</span></span>

<span data-ttu-id="a7bd7-215">Этот метод вызывается после того, как пользователь выберет элемент, непосредственно перед закрытием диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="a7bd7-216">После закрытия диалогового окна приложение может вызвать [**ифиледиалог::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) или [**ифилеопендиалог:: unresults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="a7bd7-217">Если выбранный элемент приемлем, он может вернуть S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="a7bd7-218">В противном случае они возвращают \_ false и экранный интерфейс, сообщающий пользователю о том, почему выбранный элемент является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="a7bd7-219">Если \_ возвращается значение S false, диалоговое окно не закрывается.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="a7bd7-220">Вызывающий процесс может использовать маркер окна самого диалогового окна в качестве родительского элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="a7bd7-221">Этот маркер можно получить при первом вызове [**иолевиндов:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , а затем вызвать [**иолевиндов::**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) с маркером, как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="a7bd7-222">Оншаревиолатион и Оноверврите</span><span class="sxs-lookup"><span data-stu-id="a7bd7-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="a7bd7-223">Если пользователь выбирает перезапись файла в диалоговом окне **сохранения** или если файл, который требуется сохранить или заменить, используется и не может быть записан в (нарушение общего доступа), приложение может предоставить пользовательские функции для переопределения поведения диалогового окна по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="a7bd7-224">По умолчанию при перезаписи файла в диалоговом окне отображается запрос, позволяющий пользователю проверить это действие.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="a7bd7-225">В случае нарушения общего доступа по умолчанию в диалоговом окне отображается сообщение об ошибке, оно не закрывается и пользователь должен выбрать другой вариант.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="a7bd7-226">Вызывающий процесс может переопределить эти значения по умолчанию и при необходимости отобразить собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="a7bd7-227">В диалоговом окне можно указать отказаться от файла и оставить открытым или принять его и закрыть его успешно.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="a7bd7-228">Настройка диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a7bd7-228">Customizing the Dialog</span></span>

<span data-ttu-id="a7bd7-229">В диалоговое окно можно добавить множество элементов управления без указания шаблона диалогового окна Win32.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="a7bd7-230">К этим элементам управления относятся кнопка, ComboBox, EditBox, Чеккбуттон, списки RadioButton, группы, разделители и статические текстовые элементы управления.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="a7bd7-231">Вызовите **QueryInterface** для объекта диалогового окна ([**ифиледиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**ифилеопендиалог**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)или [**ифилесаведиалог**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)), чтобы получить указатель [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) .</span><span class="sxs-lookup"><span data-stu-id="a7bd7-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="a7bd7-232">Используйте этот интерфейс для добавления элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-232">Use that interface to add controls.</span></span> <span data-ttu-id="a7bd7-233">Каждый элемент управления имеет связанный идентификатор, предоставленный вызывающим объектом, а также *видимое* и *включенное* состояние, которое может быть задано вызывающим процессом.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="a7bd7-234">С некоторыми элементами управления, такими как кнопка, также связан текст.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="a7bd7-235">В «визуальную группу» можно добавить несколько элементов управления, которые перемещаются в виде одного элемента в макете диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="a7bd7-236">С группами может быть связана метка.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="a7bd7-237">Элементы управления можно добавлять только до отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="a7bd7-238">Однако после отображения диалогового окна элементы управления могут быть скрыты или отображены по желанию, возможно, в ответ на действия пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="a7bd7-239">В следующих примерах показано, как добавить список переключателей в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="a7bd7-240">Добавление параметров к кнопке «ОК»</span><span class="sxs-lookup"><span data-stu-id="a7bd7-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="a7bd7-241">Аналогичным образом можно добавлять варианты к кнопкам **Открыть** или **сохранить** , которые являются кнопкой **ОК** для соответствующих типов диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="a7bd7-242">Доступ к параметрам можно получить с помощью раскрывающегося списка, присоединенного к кнопке.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="a7bd7-243">Первый элемент в списке преобразуется в текст кнопки.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="a7bd7-244">В следующем примере показано, как предоставить кнопку " **Открыть** " с двумя возможностями: "Открыть" и "открыть только для чтения".</span><span class="sxs-lookup"><span data-stu-id="a7bd7-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="a7bd7-245">Выбранный пользователь может быть проверен после того, как диалоговое окно будет возвращено из метода [**показа**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) , как для поля со списком, или проверяться в ходе обработки с помощью [**Ифиледиаложевентс:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="a7bd7-246">Реагирование на события в добавленных элементах управления</span><span class="sxs-lookup"><span data-stu-id="a7bd7-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="a7bd7-247">Обработчик событий, предоставляемый вызывающим процессом, может реализовать [**ифиледиалогконтролевентс**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) в дополнение к [**ифиледиаложевентс**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span><span class="sxs-lookup"><span data-stu-id="a7bd7-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="a7bd7-248">**Ифиледиалогконтролевентс** позволяет вызывающему процессу реагировать на эти события:</span><span class="sxs-lookup"><span data-stu-id="a7bd7-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="a7bd7-249">Кнопка нажата</span><span class="sxs-lookup"><span data-stu-id="a7bd7-249">PushButton clicked</span></span>
-   <span data-ttu-id="a7bd7-250">Изменено состояние Чеккбуттон</span><span class="sxs-lookup"><span data-stu-id="a7bd7-250">CheckButton state changed</span></span>
-   <span data-ttu-id="a7bd7-251">Элемент, выбранный из списка меню, ComboBox или RadioButton</span><span class="sxs-lookup"><span data-stu-id="a7bd7-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="a7bd7-252">Управление активацией.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-252">Control activating.</span></span> <span data-ttu-id="a7bd7-253">Он отправляется, когда меню собирается отобразить раскрывающийся список, если вызывающий процесс хочет изменить элементы в списке.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="a7bd7-254">Полные примеры</span><span class="sxs-lookup"><span data-stu-id="a7bd7-254">Full Samples</span></span>

<span data-ttu-id="a7bd7-255">Ниже приведены полные, загружаемые образцы C++ из пакета средств разработки программного обеспечения (SDK) для Windows, демонстрирующие использование и взаимодействие с диалоговым окном общих элементов.</span><span class="sxs-lookup"><span data-stu-id="a7bd7-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="a7bd7-256">Пример: стандартное диалоговое окно выбора файла</span><span class="sxs-lookup"><span data-stu-id="a7bd7-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="a7bd7-257">Пример: режимы стандартного диалогового окна выбора файла</span><span class="sxs-lookup"><span data-stu-id="a7bd7-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="a7bd7-258">См. также</span><span class="sxs-lookup"><span data-stu-id="a7bd7-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7bd7-259">**IID \_ ППВ \_ args**</span><span class="sxs-lookup"><span data-stu-id="a7bd7-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 

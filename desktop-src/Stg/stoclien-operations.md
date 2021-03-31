---
title: Операции Стоклиен
description: В примере Стоклиен показано, как клиент использует структурированное хранилище. Ниже приведена сводка операций Стоклиен.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Операции Стоклиен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792949"
---
# <a name="stoclien-operations"></a><span data-ttu-id="bbfb5-105">Операции Стоклиен</span><span class="sxs-lookup"><span data-stu-id="bbfb5-105">StoClien Operations</span></span>

<span data-ttu-id="bbfb5-106">В примере [стоклиен](structured-storage-client-sample--stoclien-.md) показано, как клиент использует структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-106">The [StoClien](structured-storage-client-sample--stoclien-.md) sample demonstrates how the client uses structured storage.</span></span> <span data-ttu-id="bbfb5-107">Ниже приведена сводка операций Стоклиен.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-107">The following summarizes the StoClien operations.</span></span>

<span data-ttu-id="bbfb5-108">Клиентская область окна приложения [стоклиен](structured-storage-client-sample--stoclien-.md) используется для визуального отображения полилиний, созданных с помощью мыши или планшетного устройства.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-108">The [StoClien](structured-storage-client-sample--stoclien-.md) application window client area is used for visual display of freeform drawing created with a mouse or tablet device.</span></span> <span data-ttu-id="bbfb5-109">Для рисования с помощью мыши нажмите и удерживайте левую кнопку мыши при перемещении мыши.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-109">To draw with the mouse, press and hold the left mouse button while moving the mouse.</span></span> <span data-ttu-id="bbfb5-110">Отпуская левую кнопку мыши завершает рисование линии.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-110">Releasing the left mouse button ends the drawing of a line.</span></span>

<span data-ttu-id="bbfb5-111">Ниже приведена сводка операций с точки зрения Stoclien.exe в качестве клиента COM Stoserve.dll сервера COM:</span><span class="sxs-lookup"><span data-stu-id="bbfb5-111">Here is a summary of operations from the standpoint of Stoclien.exe as a COM client of the Stoserve.dll COM server:</span></span>

<dl> <dt>

<span data-ttu-id="bbfb5-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Файл/открыть</span><span class="sxs-lookup"><span data-stu-id="bbfb5-112"><span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>File/Open</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-113">Отображает диалоговое окно Открыть, чтобы получить имя и путь для существующего файла документа, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-113">Shows the Open dialog box to obtain a name and path for an existing paper drawing file to open.</span></span> <span data-ttu-id="bbfb5-114">Значение по умолчанию. Предполагается, что для этих файлов используется расширение имени файла PAP.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-114">A default .PAP file name extension for these files is assumed.</span></span> <span data-ttu-id="bbfb5-115">Если при выборе этого пункта меню в существующий рисунок были внесены изменения, то сначала будет отображаться отдельное диалоговое окно с запросом пользователя, если текущий рисунок должен быть сохранен в связанном с ним составном файле.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-115">If changes were made to the existing drawing when this menu item is chosen, a separate dialog will first be shown asking the user if the current drawing should be saved into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Файл/сохранить</span><span class="sxs-lookup"><span data-stu-id="bbfb5-116"><span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>File/Save</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-117">Сохраняет текущий документ в связанном составном файле.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-117">Saves the current drawing into its associated compound file.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Файл/сохранить как</span><span class="sxs-lookup"><span data-stu-id="bbfb5-118"><span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>File/Save As</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-119">Отображает диалоговое окно Сохранить как, чтобы получить имя и путь для нового создаваемого файла документа бумаги.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-119">Shows the Save As dialog box to obtain a name and path for a new paper drawing file to create.</span></span> <span data-ttu-id="bbfb5-120">Текущий рисунок преобразуется в сохраненное содержимое нового файла, а новый файл превращается в новый связанный составной файл для рисования.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-120">The current drawing becomes the saved content of the new file, and the new file becomes the new associated compound file for the drawing.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Файл или выход</span><span class="sxs-lookup"><span data-stu-id="bbfb5-121"><span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>File/Exit</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-122">Выход из [стоклиен](structured-storage-client-sample--stoclien-.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb5-122">Exits [StoClien](structured-storage-client-sample--stoclien-.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Рисование и рисование на</span><span class="sxs-lookup"><span data-stu-id="bbfb5-123"><span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Draw/Drawing On</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-124">Включает рисование между клиентом [стоклиен](structured-storage-client-sample--stoclien-.md) и объектом собумаги на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-124">Turns on drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="bbfb5-125">Эта команда блокирует объект совместной печати для монопольного использования этим клиентом и предотвращает доступ других клиентов к тому же экземпляру совместной бумаги на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-125">This command locks the COPaper object for exclusive use by this client and prevents other clients from accessing the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Рисование и рисование</span><span class="sxs-lookup"><span data-stu-id="bbfb5-126"><span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Draw/Drawing Off</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-127">Отключает Рисование между клиентом [стоклиен](structured-storage-client-sample--stoclien-.md) и объектом собумаги на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-127">Turns off drawing between the [StoClien](structured-storage-client-sample--stoclien-.md) client and the COPaper object in the server.</span></span> <span data-ttu-id="bbfb5-128">Эта команда разблокирует собумагу для монопольного использования этим клиентом и позволяет другим клиентам получить доступ к тому же экземпляру совместной бумаги на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-128">This command unlocks the COPaper for exclusive use by this client and allows other clients to access the same COPaper instance in the server.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Рисование и перерисовка</span><span class="sxs-lookup"><span data-stu-id="bbfb5-129"><span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Draw/Redraw</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-130">Перерисовывает в клиенте текущие данные рисования, удерживаемые в объекте собумаги на сервере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-130">Redraws in the client the current drawing data held in the COPaper object in the server.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Рисование и стирание</span><span class="sxs-lookup"><span data-stu-id="bbfb5-131"><span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Draw/Erase</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-132">Удаляет текущее содержимое рисунка и очищает изображение окна.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-132">Erases the current drawing content and clears the window image.</span></span> <span data-ttu-id="bbfb5-133">Выбор в меню: перо/цвет отображает диалоговое окно Выбор цвета для получения нового цвета пера для рисования.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-133">Menu Selection: Pen/Color Shows the Choose Color dialog box to obtain a new pen color for drawing.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Перо/средний</span><span class="sxs-lookup"><span data-stu-id="bbfb5-134"><span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Pen/Medium</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-135">Выбирает среднюю ширину для рисования.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-135">Chooses the medium width for drawing.</span></span> <span data-ttu-id="bbfb5-136">Галочка в этом варианте меню означает, что средняя — это текущая ширина пера.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-136">A check mark on this menu choice indicates that medium is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Перо/толстое</span><span class="sxs-lookup"><span data-stu-id="bbfb5-137"><span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Pen/Thick</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-138">Выбирает жирную ширину для рисования.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-138">Chooses the thick width for drawing.</span></span> <span data-ttu-id="bbfb5-139">Галочка в этом варианте меню означает, что жирная ширина является текущей толщиной пера.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-139">A check mark on this menu choice indicates that thick is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Перо или тонкий</span><span class="sxs-lookup"><span data-stu-id="bbfb5-140"><span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Pen/Thin</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-141">Выбирает тонкую ширину для рисования.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-141">Chooses the thin width for drawing.</span></span> <span data-ttu-id="bbfb5-142">Галочка в этом меню указывает на то, что тонкий цвет является текущей толщиной пера.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-142">A check mark on this menu choice indicates that thin is the current pen width.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Приемник/подключение</span><span class="sxs-lookup"><span data-stu-id="bbfb5-143"><span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Sink/Connect</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-144">Подключает интерфейс Копаперсинк Ипаперсинк к точке подключения объекта кобумага Паперсинк.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-144">Connects the COPaperSink IPaperSink interface to the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="bbfb5-145">Перерисовка текущего изображения рисунка в [стоклиен](structured-storage-client-sample--stoclien-.md) полагается на соединение приемника.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-145">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="bbfb5-146">Галочка в этом варианте меню означает, что перерисовка подключена.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-146">A check mark on this menu choice indicates that repainting is connected.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Приемник/отключение</span><span class="sxs-lookup"><span data-stu-id="bbfb5-147"><span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Sink/Disconnect</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-148">Отключает интерфейс Копаперсинк Ипаперсинк от объекта кодокументной Паперсинк точки подключения.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-148">Disconnects the COPaperSink IPaperSink interface from the COPaper object PaperSink connection point.</span></span> <span data-ttu-id="bbfb5-149">Перерисовка текущего изображения рисунка в [стоклиен](structured-storage-client-sample--stoclien-.md) полагается на соединение приемника.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-149">Repainting of the current drawing image in [StoClien](structured-storage-client-sample--stoclien-.md) relies on the sink connection.</span></span> <span data-ttu-id="bbfb5-150">Галочка в этом варианте меню означает, что перерисовка отключена.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-150">A check mark on this menu choice indicates that repainting is disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Руководство по справке и Стоклиен</span><span class="sxs-lookup"><span data-stu-id="bbfb5-151"><span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Help/StoClien Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-152">Открывает STOCLIEN.HTM файл учебника в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-152">Opens the STOCLIEN.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Руководство по справке и Стосерве</span><span class="sxs-lookup"><span data-stu-id="bbfb5-153"><span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Help/StoServe Tutorial</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-154">Открывает STOSERVE.HTM файл учебника в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-154">Opens the STOSERVE.HTM tutorial file in the Web browser.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Файл исходного кода справки или чтения</span><span class="sxs-lookup"><span data-stu-id="bbfb5-155"><span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Help/Read Source File</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-156">Открывает диалоговое окно Открыть, в котором можно открыть исходный файл из этого занятия или другого файла в блокноте Windows.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-156">Displays the Open dialog box so you can open a source file from this lesson or another one in the Windows Notepad.</span></span>

</dd> <dt>

<span data-ttu-id="bbfb5-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Справка/о Стоклиен</span><span class="sxs-lookup"><span data-stu-id="bbfb5-157"><span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Help/About StoClien</span></span>
</dt> <dd>

<span data-ttu-id="bbfb5-158">Отображает диалоговое окно "о программе" для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-158">Displays the About dialog box for this application.</span></span>

</dd> </dl>

<span data-ttu-id="bbfb5-159">В примере [стоклиен](structured-storage-client-sample--stoclien-.md) используются многие служебные классы и службы, предоставляемые [аппутил](./using-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb5-159">The [StoClien](structured-storage-client-sample--stoclien-.md) sample uses many of the utility classes and services provided by [APPUTIL](./using-visual-studio.md).</span></span> <span data-ttu-id="bbfb5-160">Дополнительные сведения о [аппутил](./using-visual-studio.md)см. в разделе исходный код библиотеки [аппутил](./using-visual-studio.md) в каталоге одноуровневых [аппутил](./using-visual-studio.md) и Apputil.md в главном каталоге Tutorial.</span><span class="sxs-lookup"><span data-stu-id="bbfb5-160">For more information about [APPUTIL](./using-visual-studio.md), see the [APPUTIL](./using-visual-studio.md) library source code in the sibling [APPUTIL](./using-visual-studio.md) directory and Apputil.md in the main tutorial directory.</span></span> <span data-ttu-id="bbfb5-161">Дополнительные сведения о [аппутил](./using-visual-studio.md)см. [в разделе Создание образцов](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb5-161">For more information about [APPUTIL](./using-visual-studio.md), see [How to Build Samples](how-to-build-samples.md).</span></span>

 

 
---
description: Таблица классов содержит сведения, относящиеся к серверу COM, которые должны быть созданы как часть объявления продукта. Каждая строка может формировать набор разделов и значений реестра. В эту таблицу включено сопоставленные сведения ProgId.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Таблица классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662901"
---
# <a name="class-table"></a><span data-ttu-id="25470-105">Таблица классов</span><span class="sxs-lookup"><span data-stu-id="25470-105">Class Table</span></span>

<span data-ttu-id="25470-106">Таблица классов содержит сведения, относящиеся к серверу COM, которые должны быть созданы как часть объявления продукта.</span><span class="sxs-lookup"><span data-stu-id="25470-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="25470-107">Каждая строка может формировать набор разделов и значений реестра.</span><span class="sxs-lookup"><span data-stu-id="25470-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="25470-108">В эту таблицу включено сопоставленные сведения ProgId.</span><span class="sxs-lookup"><span data-stu-id="25470-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="25470-109">Таблица классов содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="25470-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="25470-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="25470-110">Column</span></span>           | <span data-ttu-id="25470-111">Type</span><span class="sxs-lookup"><span data-stu-id="25470-111">Type</span></span>                         | <span data-ttu-id="25470-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="25470-112">Key</span></span> | <span data-ttu-id="25470-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="25470-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="25470-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="25470-114">CLSID</span></span>            | [<span data-ttu-id="25470-115">GUID</span><span class="sxs-lookup"><span data-stu-id="25470-115">GUID</span></span>](guid.md)             | <span data-ttu-id="25470-116">Да</span><span class="sxs-lookup"><span data-stu-id="25470-116">Y</span></span>   | <span data-ttu-id="25470-117">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-117">N</span></span>        |
| <span data-ttu-id="25470-118">Контекст</span><span class="sxs-lookup"><span data-stu-id="25470-118">Context</span></span>          | [<span data-ttu-id="25470-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="25470-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="25470-120">Да</span><span class="sxs-lookup"><span data-stu-id="25470-120">Y</span></span>   | <span data-ttu-id="25470-121">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-121">N</span></span>        |
| <span data-ttu-id="25470-122">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="25470-122">Component\_</span></span>      | [<span data-ttu-id="25470-123">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="25470-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="25470-124">Да</span><span class="sxs-lookup"><span data-stu-id="25470-124">Y</span></span>   | <span data-ttu-id="25470-125">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-125">N</span></span>        |
| <span data-ttu-id="25470-126">ProgId \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="25470-126">ProgId\_Default</span></span>  | [<span data-ttu-id="25470-127">Text</span><span class="sxs-lookup"><span data-stu-id="25470-127">Text</span></span>](text.md)             | <span data-ttu-id="25470-128">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-128">N</span></span>   | <span data-ttu-id="25470-129">Да</span><span class="sxs-lookup"><span data-stu-id="25470-129">Y</span></span>        |
| <span data-ttu-id="25470-130">Описание</span><span class="sxs-lookup"><span data-stu-id="25470-130">Description</span></span>      | [<span data-ttu-id="25470-131">Text</span><span class="sxs-lookup"><span data-stu-id="25470-131">Text</span></span>](text.md)             | <span data-ttu-id="25470-132">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-132">N</span></span>   | <span data-ttu-id="25470-133">Да</span><span class="sxs-lookup"><span data-stu-id="25470-133">Y</span></span>        |
| <span data-ttu-id="25470-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="25470-134">AppId\_</span></span>          | [<span data-ttu-id="25470-135">GUID</span><span class="sxs-lookup"><span data-stu-id="25470-135">GUID</span></span>](guid.md)             | <span data-ttu-id="25470-136">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-136">N</span></span>   | <span data-ttu-id="25470-137">Да</span><span class="sxs-lookup"><span data-stu-id="25470-137">Y</span></span>        |
| <span data-ttu-id="25470-138">филетипемаск</span><span class="sxs-lookup"><span data-stu-id="25470-138">FileTypeMask</span></span>     | [<span data-ttu-id="25470-139">Text</span><span class="sxs-lookup"><span data-stu-id="25470-139">Text</span></span>](text.md)             | <span data-ttu-id="25470-140">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-140">N</span></span>   | <span data-ttu-id="25470-141">Да</span><span class="sxs-lookup"><span data-stu-id="25470-141">Y</span></span>        |
| <span data-ttu-id="25470-142">Значок\_</span><span class="sxs-lookup"><span data-stu-id="25470-142">Icon\_</span></span>           | [<span data-ttu-id="25470-143">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="25470-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="25470-144">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-144">N</span></span>   | <span data-ttu-id="25470-145">Да</span><span class="sxs-lookup"><span data-stu-id="25470-145">Y</span></span>        |
| <span data-ttu-id="25470-146">икониндекс</span><span class="sxs-lookup"><span data-stu-id="25470-146">IconIndex</span></span>        | [<span data-ttu-id="25470-147">Integer</span><span class="sxs-lookup"><span data-stu-id="25470-147">Integer</span></span>](integer.md)       | <span data-ttu-id="25470-148">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-148">N</span></span>   | <span data-ttu-id="25470-149">Да</span><span class="sxs-lookup"><span data-stu-id="25470-149">Y</span></span>        |
| <span data-ttu-id="25470-150">дефинпрочандлер</span><span class="sxs-lookup"><span data-stu-id="25470-150">DefInprocHandler</span></span> | [<span data-ttu-id="25470-151">Имя файла</span><span class="sxs-lookup"><span data-stu-id="25470-151">Filename</span></span>](filename.md)     | <span data-ttu-id="25470-152">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-152">N</span></span>   | <span data-ttu-id="25470-153">Да</span><span class="sxs-lookup"><span data-stu-id="25470-153">Y</span></span>        |
| <span data-ttu-id="25470-154">Аргумент</span><span class="sxs-lookup"><span data-stu-id="25470-154">Argument</span></span>         | [<span data-ttu-id="25470-155">Формате</span><span class="sxs-lookup"><span data-stu-id="25470-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="25470-156">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-156">N</span></span>   | <span data-ttu-id="25470-157">Да</span><span class="sxs-lookup"><span data-stu-id="25470-157">Y</span></span>        |
| <span data-ttu-id="25470-158">Функция\_</span><span class="sxs-lookup"><span data-stu-id="25470-158">Feature\_</span></span>        | [<span data-ttu-id="25470-159">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="25470-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="25470-160">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-160">N</span></span>   | <span data-ttu-id="25470-161">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-161">N</span></span>        |
| <span data-ttu-id="25470-162">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="25470-162">Attributes</span></span>       | [<span data-ttu-id="25470-163">Integer</span><span class="sxs-lookup"><span data-stu-id="25470-163">Integer</span></span>](integer.md)       | <span data-ttu-id="25470-164">Нет</span><span class="sxs-lookup"><span data-stu-id="25470-164">N</span></span>   | <span data-ttu-id="25470-165">Да</span><span class="sxs-lookup"><span data-stu-id="25470-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="25470-166">Сведения о столбце</span><span class="sxs-lookup"><span data-stu-id="25470-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="25470-167"><span id="CLSID"></span><span id="clsid"></span>ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="25470-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="25470-168">Идентификатор класса (ID) сервера COM.</span><span class="sxs-lookup"><span data-stu-id="25470-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="25470-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Локального</span><span class="sxs-lookup"><span data-stu-id="25470-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="25470-170">Контекст сервера для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="25470-170">The server context for this server.</span></span> <span data-ttu-id="25470-171">Введите одно из следующих значений для ключа CLSID.</span><span class="sxs-lookup"><span data-stu-id="25470-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="25470-172">КЛЮЧ CLSID</span><span class="sxs-lookup"><span data-stu-id="25470-172">CLSID KEY</span></span>                             | <span data-ttu-id="25470-173">Описание</span><span class="sxs-lookup"><span data-stu-id="25470-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="25470-174">локалсервер</span><span class="sxs-lookup"><span data-stu-id="25470-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="25470-175">Указывает полный путь к 16-разрядному приложению локального сервера.</span><span class="sxs-lookup"><span data-stu-id="25470-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="25470-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="25470-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="25470-177">Указывает полный путь к 32-битному локальному серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="25470-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="25470-178">инпроксервер</span><span class="sxs-lookup"><span data-stu-id="25470-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="25470-179">Указывает путь к DLL-библиотеке внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="25470-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="25470-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="25470-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="25470-181">Указывает путь к 32-разрядному серверу обработки и потоковой модели.</span><span class="sxs-lookup"><span data-stu-id="25470-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="25470-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="25470-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="25470-183">Внешний ключ в [таблице Component](component-table.md) , указывающий компонент, файл ключа которого предоставляет сервер COM.</span><span class="sxs-lookup"><span data-stu-id="25470-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="25470-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="25470-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="25470-185">Идентификатор программы по умолчанию, связанный с этим ИДЕНТИФИКАТОРом класса.</span><span class="sxs-lookup"><span data-stu-id="25470-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="25470-186">Этот столбец является внешним ключом в [таблице ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="25470-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="25470-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="25470-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="25470-188">Локализованное описание, связанное с ИДЕНТИФИКАТОРом класса и ИДЕНТИФИКАТОРом программы.</span><span class="sxs-lookup"><span data-stu-id="25470-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="25470-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>ИД\_</span><span class="sxs-lookup"><span data-stu-id="25470-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="25470-190">Идентификатор приложения, содержащего сведения DCOM для связанного приложения (строка [GUID](guid.md)).</span><span class="sxs-lookup"><span data-stu-id="25470-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="25470-191">Этот столбец является внешним ключом в [таблице AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="25470-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="25470-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>филетипемаск</span><span class="sxs-lookup"><span data-stu-id="25470-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="25470-193">Содержит сведения для ключа HKCR (this CLSID).</span><span class="sxs-lookup"><span data-stu-id="25470-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="25470-194">Если существует несколько шаблонов, они должны быть заключены в точку с запятой, а числовые подразделы будут созданы: 0, 1, 2... Дополнительные сведения об этих функциях см. в разделе [**жетклассфиле**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="25470-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="25470-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Значок\_</span><span class="sxs-lookup"><span data-stu-id="25470-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="25470-196">Файл, предоставляющий значок, связанный с этим идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="25470-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="25470-197">Установщик записывает запись в этот столбец в раздел Дефаултикон, связанный с ProgId.</span><span class="sxs-lookup"><span data-stu-id="25470-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="25470-198">Если значение не равно null, то столбец является внешним ключом в [таблице значков](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="25470-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="25470-199">Если значение равно null, COM-сервер предоставляет ресурс значка.</span><span class="sxs-lookup"><span data-stu-id="25470-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="25470-200">Для правильного вывода привязок объявленных файлов и сочетаний клавиш в этом столбце требуется значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="25470-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="25470-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>икониндекс</span><span class="sxs-lookup"><span data-stu-id="25470-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="25470-202">Индекс значка в файле значка.</span><span class="sxs-lookup"><span data-stu-id="25470-202">Icon index into the icon file.</span></span> <span data-ttu-id="25470-203">Может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="25470-203">This can be null.</span></span>

<span data-ttu-id="25470-204">Только неотрицательные числа.</span><span class="sxs-lookup"><span data-stu-id="25470-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="25470-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>дефинпрочандлер</span><span class="sxs-lookup"><span data-stu-id="25470-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="25470-206">В этом поле указывается внутрипроцессный обработчик по умолчанию для контекста сервера, указанного в поле контекста.</span><span class="sxs-lookup"><span data-stu-id="25470-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="25470-207">Это поле должно иметь значение null, если в поле контекста отображается ключ CLSID Инпроксервер или Инпроксервер.</span><span class="sxs-lookup"><span data-stu-id="25470-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="25470-208">Если в поле контекста отображается ключ CLSID Локалсервер или LocalServer32, значение в поле Дефинпрочандлер идентифицирует обработчик по умолчанию в процессе.</span><span class="sxs-lookup"><span data-stu-id="25470-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="25470-209">Значение</span><span class="sxs-lookup"><span data-stu-id="25470-209">Value</span></span>                | <span data-ttu-id="25470-210">Описание</span><span class="sxs-lookup"><span data-stu-id="25470-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25470-211">нечисловое значение</span><span class="sxs-lookup"><span data-stu-id="25470-211">non-numeric value</span></span>    | <span data-ttu-id="25470-212">Установщик рассматривает нечисловое значение в поле Дефинпрочандлер в качестве системного файла, обслуживающего как 32-разрядный внутрипроцессный обработчик, заданный ключом InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="25470-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="25470-213">NULL</span><span class="sxs-lookup"><span data-stu-id="25470-213">Null</span></span>                 | <span data-ttu-id="25470-214">Поля Дефинпрочандлер и Argument могут иметь значение NULL для ключа CLSID Локалсервер или LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="25470-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="25470-215">1 = по умолчанию (система)</span><span class="sxs-lookup"><span data-stu-id="25470-215">1 = default (system)</span></span> | <span data-ttu-id="25470-216">По умолчанию используется 16-разрядный внутрипроцессный обработчик, заданный параметром Инпрочандлер.</span><span class="sxs-lookup"><span data-stu-id="25470-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="25470-217">В этом случае значение Инпрочандлер является именем в реестре, в котором хранится значение внутрипроцессного обработчика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25470-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="25470-218">Например, в HKEY \_ \_ \\ классы программного обеспечения для локального компьютера см \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="25470-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="25470-219">2 = по умолчанию (система)</span><span class="sxs-lookup"><span data-stu-id="25470-219">2 = default (system)</span></span> | <span data-ttu-id="25470-220">Значение по умолчанию — это 32-разрядный внутрипроцессный обработчик, заданный параметром InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="25470-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="25470-221">В этом случае значение InprocHandler32 является именем в реестре, в котором хранится значение внутрипроцессного обработчика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25470-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="25470-222">Например, в HKEY \_ \_ \\ классы программного обеспечения для локального компьютера см \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="25470-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="25470-223">3 = по умолчанию (система)</span><span class="sxs-lookup"><span data-stu-id="25470-223">3 = default (system)</span></span> | <span data-ttu-id="25470-224">Значение по умолчанию — 16-разрядный или 32-разрядный внутрипроцессный обработчик.</span><span class="sxs-lookup"><span data-stu-id="25470-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="25470-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Параметр</span><span class="sxs-lookup"><span data-stu-id="25470-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="25470-226">Если в поле контекста отображается ключ CLSID Локалсервер или LocalServer32, то текст в этом поле регистрируется в качестве аргумента для сервера и используется COM для вызова сервера.</span><span class="sxs-lookup"><span data-stu-id="25470-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="25470-227">Поля Дефинпрочандлер и Argument могут иметь значение null, если в поле контекста отображается Локалсервер или LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="25470-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="25470-228">Обратите внимание, что разрешение свойств в поле Argument ограничено.</span><span class="sxs-lookup"><span data-stu-id="25470-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="25470-229">Свойство, отформатированное как \[ свойство \] в этом поле, может быть разрешено только в том случае, если свойство уже имеет предполагаемое значение при установке компонента, владеющего классом.</span><span class="sxs-lookup"><span data-stu-id="25470-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="25470-230">Например, для аргумента " \[ \#MyDoc.doc\] ", чтобы разрешить правильное значение, один и тот же процесс должен установить файл MyDoc.doc и компонент, владеющий этим классом.</span><span class="sxs-lookup"><span data-stu-id="25470-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="25470-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="25470-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="25470-232">Внешний ключ в [таблицу функций](feature-table.md) , указывающий компонент, предоставляющий COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="25470-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="25470-233">Внешний ключ к столбцу в одной из таблиц компонентов.</span><span class="sxs-lookup"><span data-stu-id="25470-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="25470-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибута</span><span class="sxs-lookup"><span data-stu-id="25470-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="25470-235">Если в этом столбце задано значение **мсидбклассаттрибутесрелативепас** , то для серверов COM можно использовать имя исходного файла.</span><span class="sxs-lookup"><span data-stu-id="25470-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="25470-236">Установщик регистрирует только имя файла, а не полный путь.</span><span class="sxs-lookup"><span data-stu-id="25470-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="25470-237">Это позволяет серверу в текущем каталоге иметь приоритет и допускает несколько копий одного и того же компонента.</span><span class="sxs-lookup"><span data-stu-id="25470-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="25470-238">attribute</span><span class="sxs-lookup"><span data-stu-id="25470-238">Attribute</span></span>                            | <span data-ttu-id="25470-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="25470-239">Decimal</span></span> | <span data-ttu-id="25470-240">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="25470-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="25470-241">**мсидбклассаттрибутесрелативепас**</span><span class="sxs-lookup"><span data-stu-id="25470-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="25470-242">1</span><span class="sxs-lookup"><span data-stu-id="25470-242">1</span></span>       | <span data-ttu-id="25470-243">0x001</span><span class="sxs-lookup"><span data-stu-id="25470-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25470-244">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25470-244">Remarks</span></span>

<span data-ttu-id="25470-245">Эта таблица упоминается при выполнении [действия регистерклассинфо](registerclassinfo-action.md) или [унрегистерклассинфо](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="25470-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="25470-246">Проверка</span><span class="sxs-lookup"><span data-stu-id="25470-246">Validation</span></span>

<dl>

[<span data-ttu-id="25470-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="25470-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="25470-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="25470-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="25470-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="25470-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="25470-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="25470-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="25470-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="25470-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="25470-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="25470-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="25470-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="25470-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="25470-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="25470-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="25470-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="25470-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="25470-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="25470-256">ICE69</span></span>](ice69.md)  
</dl>

 

 

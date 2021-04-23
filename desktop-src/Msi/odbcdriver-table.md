---
description: В таблице Одбкдривер перечислены драйверы ODBC, принадлежащие установке.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Таблица Одбкдривер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541066"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="53b01-103">Таблица Одбкдривер</span><span class="sxs-lookup"><span data-stu-id="53b01-103">ODBCDriver Table</span></span>

<span data-ttu-id="53b01-104">В таблице Одбкдривер перечислены драйверы ODBC, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="53b01-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="53b01-105">Таблица Одбкдривер содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="53b01-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="53b01-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="53b01-106">Column</span></span>      | <span data-ttu-id="53b01-107">Type</span><span class="sxs-lookup"><span data-stu-id="53b01-107">Type</span></span>                         | <span data-ttu-id="53b01-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="53b01-108">Key</span></span> | <span data-ttu-id="53b01-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="53b01-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="53b01-110">Драйвер</span><span class="sxs-lookup"><span data-stu-id="53b01-110">Driver</span></span>      | [<span data-ttu-id="53b01-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="53b01-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="53b01-112">Да</span><span class="sxs-lookup"><span data-stu-id="53b01-112">Y</span></span>   | <span data-ttu-id="53b01-113">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-113">N</span></span>        |
| <span data-ttu-id="53b01-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="53b01-114">Component\_</span></span> | [<span data-ttu-id="53b01-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="53b01-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="53b01-116">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-116">N</span></span>   | <span data-ttu-id="53b01-117">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-117">N</span></span>        |
| <span data-ttu-id="53b01-118">Описание</span><span class="sxs-lookup"><span data-stu-id="53b01-118">Description</span></span> | [<span data-ttu-id="53b01-119">Text</span><span class="sxs-lookup"><span data-stu-id="53b01-119">Text</span></span>](text.md)             | <span data-ttu-id="53b01-120">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-120">N</span></span>   | <span data-ttu-id="53b01-121">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-121">N</span></span>        |
| <span data-ttu-id="53b01-122">Файл\_</span><span class="sxs-lookup"><span data-stu-id="53b01-122">File\_</span></span>      | [<span data-ttu-id="53b01-123">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="53b01-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="53b01-124">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-124">N</span></span>   | <span data-ttu-id="53b01-125">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-125">N</span></span>        |
| <span data-ttu-id="53b01-126">\_Настройка файла</span><span class="sxs-lookup"><span data-stu-id="53b01-126">File\_Setup</span></span> | [<span data-ttu-id="53b01-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="53b01-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="53b01-128">Нет</span><span class="sxs-lookup"><span data-stu-id="53b01-128">N</span></span>   | <span data-ttu-id="53b01-129">Да</span><span class="sxs-lookup"><span data-stu-id="53b01-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="53b01-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="53b01-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="53b01-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Аудиодрайвера</span><span class="sxs-lookup"><span data-stu-id="53b01-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="53b01-132">Имя внутреннего маркера для драйвера.</span><span class="sxs-lookup"><span data-stu-id="53b01-132">Internal token name for driver.</span></span> <span data-ttu-id="53b01-133">Первичный ключ для таблицы</span><span class="sxs-lookup"><span data-stu-id="53b01-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="53b01-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="53b01-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="53b01-135">Внешний ключ в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="53b01-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="53b01-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="53b01-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="53b01-137">Описание, зарегистрированное для этого драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="53b01-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="53b01-138">Это значение не может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="53b01-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="53b01-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="53b01-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="53b01-140">DLL-файл для драйверов, перечисленных в столбце драйвер.</span><span class="sxs-lookup"><span data-stu-id="53b01-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="53b01-141">Столбец File \_ является внешним ключом в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="53b01-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="53b01-142">Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла.</span><span class="sxs-lookup"><span data-stu-id="53b01-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="53b01-143">Синтаксис СФН \| лфн использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="53b01-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="53b01-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Настройка файла</span><span class="sxs-lookup"><span data-stu-id="53b01-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="53b01-145">Файл DLL установки драйвера, если он отличается от драйвера.</span><span class="sxs-lookup"><span data-stu-id="53b01-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="53b01-146">Столбец File \_ является внешним ключом в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="53b01-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="53b01-147">Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла.</span><span class="sxs-lookup"><span data-stu-id="53b01-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="53b01-148">Синтаксис СФН \| лфн использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="53b01-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53b01-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53b01-149">Remarks</span></span>

<span data-ttu-id="53b01-150">Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="53b01-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="53b01-151">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="53b01-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="53b01-152">Проверка</span><span class="sxs-lookup"><span data-stu-id="53b01-152">Validation</span></span>

<dl>

[<span data-ttu-id="53b01-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="53b01-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="53b01-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="53b01-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="53b01-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="53b01-155">ICE32</span></span>](ice32.md)  
</dl>

 

 




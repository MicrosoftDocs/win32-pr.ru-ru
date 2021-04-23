---
description: В таблице Одбктранслатор перечислены трансляторы ODBC, принадлежащие установке.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Таблица Одбктранслатор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651168"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="eb388-103">Таблица Одбктранслатор</span><span class="sxs-lookup"><span data-stu-id="eb388-103">ODBCTranslator Table</span></span>

<span data-ttu-id="eb388-104">В таблице Одбктранслатор перечислены трансляторы ODBC, принадлежащие установке.</span><span class="sxs-lookup"><span data-stu-id="eb388-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="eb388-105">Таблица Одбктранслатор содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="eb388-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="eb388-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="eb388-106">Column</span></span>      | <span data-ttu-id="eb388-107">Type</span><span class="sxs-lookup"><span data-stu-id="eb388-107">Type</span></span>                         | <span data-ttu-id="eb388-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="eb388-108">Key</span></span> | <span data-ttu-id="eb388-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="eb388-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="eb388-110">Переводчик</span><span class="sxs-lookup"><span data-stu-id="eb388-110">Translator</span></span>  | [<span data-ttu-id="eb388-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="eb388-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="eb388-112">Да</span><span class="sxs-lookup"><span data-stu-id="eb388-112">Y</span></span>   | <span data-ttu-id="eb388-113">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-113">N</span></span>        |
| <span data-ttu-id="eb388-114">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="eb388-114">Component\_</span></span> | [<span data-ttu-id="eb388-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="eb388-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="eb388-116">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-116">N</span></span>   | <span data-ttu-id="eb388-117">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-117">N</span></span>        |
| <span data-ttu-id="eb388-118">Описание</span><span class="sxs-lookup"><span data-stu-id="eb388-118">Description</span></span> | [<span data-ttu-id="eb388-119">Text</span><span class="sxs-lookup"><span data-stu-id="eb388-119">Text</span></span>](text.md)             | <span data-ttu-id="eb388-120">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-120">N</span></span>   | <span data-ttu-id="eb388-121">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-121">N</span></span>        |
| <span data-ttu-id="eb388-122">Файл\_</span><span class="sxs-lookup"><span data-stu-id="eb388-122">File\_</span></span>      | [<span data-ttu-id="eb388-123">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="eb388-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="eb388-124">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-124">N</span></span>   | <span data-ttu-id="eb388-125">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-125">N</span></span>        |
| <span data-ttu-id="eb388-126">\_Настройка файла</span><span class="sxs-lookup"><span data-stu-id="eb388-126">File\_Setup</span></span> | [<span data-ttu-id="eb388-127">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="eb388-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="eb388-128">Нет</span><span class="sxs-lookup"><span data-stu-id="eb388-128">N</span></span>   | <span data-ttu-id="eb388-129">Да</span><span class="sxs-lookup"><span data-stu-id="eb388-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="eb388-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="eb388-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="eb388-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="eb388-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="eb388-132">Имя внутреннего маркера для переводчика.</span><span class="sxs-lookup"><span data-stu-id="eb388-132">Internal token name for translator.</span></span> <span data-ttu-id="eb388-133">Первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="eb388-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="eb388-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="eb388-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="eb388-135">Внешний ключ в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="eb388-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="eb388-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="eb388-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="eb388-137">Описание, зарегистрированное для этого транслятора драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="eb388-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="eb388-138">Это значение не может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="eb388-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="eb388-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="eb388-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="eb388-140">DLL-файл для перемещения, указанный в столбце Translator.</span><span class="sxs-lookup"><span data-stu-id="eb388-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="eb388-141">Столбец File \_ является внешним ключом в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb388-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="eb388-142">Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла.</span><span class="sxs-lookup"><span data-stu-id="eb388-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="eb388-143">Синтаксис СФН \| лфн использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="eb388-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="eb388-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Настройка файла</span><span class="sxs-lookup"><span data-stu-id="eb388-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="eb388-145">Файл DLL установки для транслятора, если он отличается от столбца Translator.</span><span class="sxs-lookup"><span data-stu-id="eb388-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="eb388-146">Столбец File \_ является внешним ключом в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb388-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="eb388-147">Имя файла, указанное в столбце filename этой записи таблицы файлов, должно быть указано в коротком формате имени файла.</span><span class="sxs-lookup"><span data-stu-id="eb388-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="eb388-148">Синтаксис СФН \| лфн использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="eb388-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb388-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb388-149">Remarks</span></span>

<span data-ttu-id="eb388-150">Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="eb388-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="eb388-151">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb388-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="eb388-152">Проверка</span><span class="sxs-lookup"><span data-stu-id="eb388-152">Validation</span></span>

<dl>

[<span data-ttu-id="eb388-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="eb388-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="eb388-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="eb388-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="eb388-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="eb388-155">ICE32</span></span>](ice32.md)  
</dl>

 

 




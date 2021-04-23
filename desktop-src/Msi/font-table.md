---
description: Таблица Font содержит сведения для регистрации файлов шрифтов в системе.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Таблица шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998815"
---
# <a name="font-table"></a><span data-ttu-id="1f31b-103">Таблица шрифтов</span><span class="sxs-lookup"><span data-stu-id="1f31b-103">Font Table</span></span>

<span data-ttu-id="1f31b-104">Таблица Font содержит сведения для регистрации файлов шрифтов в системе.</span><span class="sxs-lookup"><span data-stu-id="1f31b-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="1f31b-105">Таблица Font содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="1f31b-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="1f31b-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="1f31b-106">Column</span></span>    | <span data-ttu-id="1f31b-107">Type</span><span class="sxs-lookup"><span data-stu-id="1f31b-107">Type</span></span>                         | <span data-ttu-id="1f31b-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="1f31b-108">Key</span></span> | <span data-ttu-id="1f31b-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="1f31b-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="1f31b-110">Файл\_</span><span class="sxs-lookup"><span data-stu-id="1f31b-110">File\_</span></span>    | [<span data-ttu-id="1f31b-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="1f31b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="1f31b-112">Да</span><span class="sxs-lookup"><span data-stu-id="1f31b-112">Y</span></span>   | <span data-ttu-id="1f31b-113">Нет</span><span class="sxs-lookup"><span data-stu-id="1f31b-113">N</span></span>        |
| <span data-ttu-id="1f31b-114">фонттитле</span><span class="sxs-lookup"><span data-stu-id="1f31b-114">FontTitle</span></span> | [<span data-ttu-id="1f31b-115">Text</span><span class="sxs-lookup"><span data-stu-id="1f31b-115">Text</span></span>](text.md)             | <span data-ttu-id="1f31b-116">Нет</span><span class="sxs-lookup"><span data-stu-id="1f31b-116">N</span></span>   | <span data-ttu-id="1f31b-117">Да</span><span class="sxs-lookup"><span data-stu-id="1f31b-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1f31b-118">Столбцы</span><span class="sxs-lookup"><span data-stu-id="1f31b-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1f31b-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="1f31b-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="1f31b-120">Внешний ключ в записи [таблицы файлов](file-table.md) для файла шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="1f31b-121">Рекомендуется, чтобы компонент, содержащий файл шрифта, имел Фонтсфолдер, указанный в \_ столбце Directory [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="1f31b-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f31b-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>фонттитле</span><span class="sxs-lookup"><span data-stu-id="1f31b-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="1f31b-123">Имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-123">Font name.</span></span> <span data-ttu-id="1f31b-124">Рекомендуется оставлять этот столбец пустым для шрифтов TrueType и наборов TrueType, поскольку установщик может зарегистрировать шрифт после считывания правильного названия шрифта из файла шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="1f31b-125">Если указано имя шрифта, оно должно быть идентично названию шрифта в файле шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="1f31b-126">Необходимо указать название для шрифтов, у которых нет внедренных имен, таких как FON-файлы.</span><span class="sxs-lookup"><span data-stu-id="1f31b-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f31b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f31b-127">Remarks</span></span>

<span data-ttu-id="1f31b-128">Эта таблица упоминается при выполнении [действия регистерфонтс](registerfonts-action.md) или [унрегистерфонтс](unregisterfonts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="1f31b-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="1f31b-129">Если поле Фонттитле оставлено пустым, имя шрифта считывается непосредственно из указанного файла шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="1f31b-130">Если имя шрифта, записанное в поле Фонттитле, отличается от внутреннего названия шрифта, записанного в файле шрифта, шрифт регистрируется дважды [действием регистерфонтс](registerfonts-action.md).</span><span class="sxs-lookup"><span data-stu-id="1f31b-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="1f31b-131">Файлы шрифтов не должны создаваться с использованием идентификатора языка, так как шрифты не содержат внедренный ресурс идентификатора языка. Поэтому столбец Language [таблицы File](file-table.md) должен быть оставлен пустым для файлов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="1f31b-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="1f31b-132">Поскольку установщик не устанавливает счетчики для файлов шрифтов по умолчанию, существующие файлы шрифтов могут быть удалены вместе с компонентом при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="1f31b-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="1f31b-133">Чтобы гарантировать, что файл шрифта не удаляется, авторы могут установить флаги **мсидбкомпонентаттрибутесшареддллрефкаунт** или **мсидбкомпонентаттрибутесперманент** bit в столбце Attributes таблицы Component компонента \_ MSI \_ \_ для компонента, содержащего файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="1f31b-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="1f31b-134">Проверка</span><span class="sxs-lookup"><span data-stu-id="1f31b-134">Validation</span></span>

<dl>

[<span data-ttu-id="1f31b-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="1f31b-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1f31b-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="1f31b-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1f31b-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="1f31b-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="1f31b-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="1f31b-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="1f31b-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="1f31b-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="1f31b-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="1f31b-140">ICE60</span></span>](ice60.md)  
</dl>

 

 




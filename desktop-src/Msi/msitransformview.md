---
description: Эта временная таблица включает функцию удаления исправлений настраиваемых действий для настраиваемых действий, добавленных или обновленных с помощью исправления.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: мситрансформвиев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674153"
---
# <a name="msitransformview"></a><span data-ttu-id="0b13d-103">мситрансформвиев</span><span class="sxs-lookup"><span data-stu-id="0b13d-103">MsiTransformView</span></span>

<span data-ttu-id="0b13d-104">Эта временная таблица включает [функцию удаления исправлений настраиваемых](custom-action-patch-uninstall-option.md) действий для настраиваемых действий, добавленных или обновленных с помощью исправления.</span><span class="sxs-lookup"><span data-stu-id="0b13d-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="0b13d-105">Если исправление добавляет или обновляет пользовательское действие с атрибутом **мсидбкустомактионтипепатчунинсталл** , установщик Windows запускает новое или обновленное настраиваемое действие при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="0b13d-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="0b13d-106">Установщик Windows делает обновления из удаляемого исправления доступными для настраиваемого действия удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="0b13d-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="0b13d-107">Исправление должно включать *<PatchGUID>* таблицу мситрансформвиев, чтобы предоставить эти сведения установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="0b13d-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="0b13d-108">Сведения в этой таблице доступны для любого неявного настраиваемого действия и недоступны для отложенных настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="0b13d-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="0b13d-109">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0b13d-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="0b13d-110">[Функция удаления исправления настраиваемого действия](custom-action-patch-uninstall-option.md) доступна, начиная с установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="0b13d-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="0b13d-111">Эта таблица должна называться Мситрансформвиев *<PatchGUID>* Table, где *<PatchGUID>* — идентификатор GUID, однозначно определяющий исправление.</span><span class="sxs-lookup"><span data-stu-id="0b13d-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="0b13d-112">Таблица Мситрансформвиев *<PatchGUID>* содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="0b13d-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="0b13d-113">Столбец</span><span class="sxs-lookup"><span data-stu-id="0b13d-113">Column</span></span>  | <span data-ttu-id="0b13d-114">Type</span><span class="sxs-lookup"><span data-stu-id="0b13d-114">Type</span></span>                         | <span data-ttu-id="0b13d-115">Ключ</span><span class="sxs-lookup"><span data-stu-id="0b13d-115">Key</span></span> | <span data-ttu-id="0b13d-116">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="0b13d-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="0b13d-117">Таблица</span><span class="sxs-lookup"><span data-stu-id="0b13d-117">Table</span></span>   | [<span data-ttu-id="0b13d-118">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0b13d-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="0b13d-119">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-119">Y</span></span>   | <span data-ttu-id="0b13d-120">Нет</span><span class="sxs-lookup"><span data-stu-id="0b13d-120">N</span></span>        |
| <span data-ttu-id="0b13d-121">Столбец</span><span class="sxs-lookup"><span data-stu-id="0b13d-121">Column</span></span>  | [<span data-ttu-id="0b13d-122">Text</span><span class="sxs-lookup"><span data-stu-id="0b13d-122">Text</span></span>](text.md)             | <span data-ttu-id="0b13d-123">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-123">Y</span></span>   | <span data-ttu-id="0b13d-124">Нет</span><span class="sxs-lookup"><span data-stu-id="0b13d-124">N</span></span>        |
| <span data-ttu-id="0b13d-125">Строка</span><span class="sxs-lookup"><span data-stu-id="0b13d-125">Row</span></span>     | [<span data-ttu-id="0b13d-126">Text</span><span class="sxs-lookup"><span data-stu-id="0b13d-126">Text</span></span>](text.md)             | <span data-ttu-id="0b13d-127">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-127">Y</span></span>   | <span data-ttu-id="0b13d-128">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-128">Y</span></span>        |
| <span data-ttu-id="0b13d-129">Данные</span><span class="sxs-lookup"><span data-stu-id="0b13d-129">Data</span></span>    | [<span data-ttu-id="0b13d-130">Text</span><span class="sxs-lookup"><span data-stu-id="0b13d-130">Text</span></span>](text.md)             | <span data-ttu-id="0b13d-131">Нет</span><span class="sxs-lookup"><span data-stu-id="0b13d-131">N</span></span>   | <span data-ttu-id="0b13d-132">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-132">Y</span></span>        |
| <span data-ttu-id="0b13d-133">Текущий</span><span class="sxs-lookup"><span data-stu-id="0b13d-133">Current</span></span> | [<span data-ttu-id="0b13d-134">Text</span><span class="sxs-lookup"><span data-stu-id="0b13d-134">Text</span></span>](text.md)             | <span data-ttu-id="0b13d-135">Нет</span><span class="sxs-lookup"><span data-stu-id="0b13d-135">N</span></span>   | <span data-ttu-id="0b13d-136">Да</span><span class="sxs-lookup"><span data-stu-id="0b13d-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="0b13d-137">Столбец</span><span class="sxs-lookup"><span data-stu-id="0b13d-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="0b13d-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица</span><span class="sxs-lookup"><span data-stu-id="0b13d-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="0b13d-139">Имя измененной таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="0b13d-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="0b13d-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Рубрик</span><span class="sxs-lookup"><span data-stu-id="0b13d-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="0b13d-141">Имя измененного столбца таблицы или вставка, удаление, создание или удаление.</span><span class="sxs-lookup"><span data-stu-id="0b13d-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="0b13d-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Строки</span><span class="sxs-lookup"><span data-stu-id="0b13d-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="0b13d-143">Список значений первичного ключа, разделенных символами табуляции.</span><span class="sxs-lookup"><span data-stu-id="0b13d-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="0b13d-144">Значения NULL первичного ключа представлены одним символом пробела.</span><span class="sxs-lookup"><span data-stu-id="0b13d-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="0b13d-145">Значение NULL в этом столбце указывает на изменение схемы.</span><span class="sxs-lookup"><span data-stu-id="0b13d-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="0b13d-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="0b13d-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="0b13d-147">Data, Name потока данных или определения столбца.</span><span class="sxs-lookup"><span data-stu-id="0b13d-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="0b13d-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Данном</span><span class="sxs-lookup"><span data-stu-id="0b13d-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="0b13d-149">Текущее значение из базы данных-образца или столбец с номером.</span><span class="sxs-lookup"><span data-stu-id="0b13d-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b13d-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b13d-150">Remarks</span></span>

<span data-ttu-id="0b13d-151">Пользовательские действия удаления исправления выполняются при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="0b13d-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="0b13d-152">Они не выполняются при удалении продукта.</span><span class="sxs-lookup"><span data-stu-id="0b13d-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="0b13d-153">Используйте [параметр Удалить исправление для настраиваемого действия](custom-action-patch-uninstall-option.md) и эту таблицу, чтобы запустить пользовательский режим только при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="0b13d-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="0b13d-154">Исправление может обновить пользовательское действие, указанное в исходном пакете (MSI-файле). Чтобы запустить обновленную версию настраиваемого действия при удалении исправления, пометьте настраиваемое действие атрибутом **мсидбкустомактионтипепатчунинсталл** в исходном пакете.</span><span class="sxs-lookup"><span data-stu-id="0b13d-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 




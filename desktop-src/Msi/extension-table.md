---
description: Таблица Extension содержит сведения о серверах расширений имен файлов, которые должны быть созданы как часть объявления продукта. Каждая строка создает набор разделов и значений реестра.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Таблица расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650642"
---
# <a name="extension-table"></a><span data-ttu-id="cfee5-104">Таблица расширения</span><span class="sxs-lookup"><span data-stu-id="cfee5-104">Extension Table</span></span>

<span data-ttu-id="cfee5-105">Таблица Extension содержит сведения о серверах расширений имен файлов, которые должны быть созданы как часть объявления продукта.</span><span class="sxs-lookup"><span data-stu-id="cfee5-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="cfee5-106">Каждая строка создает набор разделов и значений реестра.</span><span class="sxs-lookup"><span data-stu-id="cfee5-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="cfee5-107">Таблица Extension содержит столбцы, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cfee5-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="cfee5-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="cfee5-108">Column</span></span>      | <span data-ttu-id="cfee5-109">Type</span><span class="sxs-lookup"><span data-stu-id="cfee5-109">Type</span></span>                         | <span data-ttu-id="cfee5-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="cfee5-110">Key</span></span> | <span data-ttu-id="cfee5-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="cfee5-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="cfee5-112">Расширение</span><span class="sxs-lookup"><span data-stu-id="cfee5-112">Extension</span></span>   | [<span data-ttu-id="cfee5-113">Text</span><span class="sxs-lookup"><span data-stu-id="cfee5-113">Text</span></span>](text.md)             | <span data-ttu-id="cfee5-114">Да</span><span class="sxs-lookup"><span data-stu-id="cfee5-114">Y</span></span>   | <span data-ttu-id="cfee5-115">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-115">N</span></span>        |
| <span data-ttu-id="cfee5-116">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-116">Component\_</span></span> | [<span data-ttu-id="cfee5-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cfee5-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="cfee5-118">Да</span><span class="sxs-lookup"><span data-stu-id="cfee5-118">Y</span></span>   | <span data-ttu-id="cfee5-119">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-119">N</span></span>        |
| <span data-ttu-id="cfee5-120">ID\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-120">ProgId\_</span></span>    | [<span data-ttu-id="cfee5-121">Text</span><span class="sxs-lookup"><span data-stu-id="cfee5-121">Text</span></span>](text.md)             | <span data-ttu-id="cfee5-122">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-122">N</span></span>   | <span data-ttu-id="cfee5-123">Да</span><span class="sxs-lookup"><span data-stu-id="cfee5-123">Y</span></span>        |
| <span data-ttu-id="cfee5-124">MIME\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-124">MIME\_</span></span>      | [<span data-ttu-id="cfee5-125">Text</span><span class="sxs-lookup"><span data-stu-id="cfee5-125">Text</span></span>](text.md)             | <span data-ttu-id="cfee5-126">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-126">N</span></span>   | <span data-ttu-id="cfee5-127">Да</span><span class="sxs-lookup"><span data-stu-id="cfee5-127">Y</span></span>        |
| <span data-ttu-id="cfee5-128">Функция\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-128">Feature\_</span></span>   | [<span data-ttu-id="cfee5-129">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="cfee5-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="cfee5-130">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-130">N</span></span>   | <span data-ttu-id="cfee5-131">Нет</span><span class="sxs-lookup"><span data-stu-id="cfee5-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cfee5-132">Столбцы</span><span class="sxs-lookup"><span data-stu-id="cfee5-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cfee5-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Продлен</span><span class="sxs-lookup"><span data-stu-id="cfee5-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="cfee5-134">Расширение, связанное со строкой таблицы.</span><span class="sxs-lookup"><span data-stu-id="cfee5-134">The extension associated with the table row.</span></span> <span data-ttu-id="cfee5-135">Длина расширения может доставлять до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="cfee5-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="cfee5-136">Введите расширение в это поле без предшествующей точки.</span><span class="sxs-lookup"><span data-stu-id="cfee5-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="cfee5-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="cfee5-138">Внешний ключ к первому столбцу таблицы [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cfee5-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="cfee5-139">Этот столбец ссылается на компонент, управляющий установкой расширения.</span><span class="sxs-lookup"><span data-stu-id="cfee5-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="cfee5-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ID\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="cfee5-141">Идентификатор программы, связанный с этим расширением.</span><span class="sxs-lookup"><span data-stu-id="cfee5-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="cfee5-142">Это внешний ключ в таблице [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cfee5-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="cfee5-143"><span id="MIME_"></span><span id="mime_"></span>ФОРМАТА\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="cfee5-144">Тип содержимого, который должен быть записан для столбца расширения.</span><span class="sxs-lookup"><span data-stu-id="cfee5-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="cfee5-145">Внешний ключ к первому столбцу таблицы [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cfee5-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="cfee5-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="cfee5-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="cfee5-147">Внешний ключ в первом столбце таблицы [Feature](feature-table.md) , указывающий компонент, предоставляющий сервер расширения.</span><span class="sxs-lookup"><span data-stu-id="cfee5-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfee5-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfee5-148">Remarks</span></span>

<span data-ttu-id="cfee5-149">Обращение к таблице расширений происходит при выполнении действия [регистерекстенсионинфо](registerextensioninfo-action.md) или [унрегистерекстенсионинфо](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cfee5-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="cfee5-150">Проверка</span><span class="sxs-lookup"><span data-stu-id="cfee5-150">Validation</span></span>

<dl>

[<span data-ttu-id="cfee5-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="cfee5-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cfee5-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="cfee5-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cfee5-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="cfee5-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="cfee5-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="cfee5-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="cfee5-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="cfee5-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="cfee5-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="cfee5-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="cfee5-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="cfee5-157">ICE69</span></span>](ice69.md)  
</dl>

 

 




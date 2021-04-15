---
description: В таблице Модуликсклусион хранится список других модулей слияния, которые несовместимы в одной базе данных установщика.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Таблица Модуликсклусион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424009"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="d2b15-103">Таблица Модуликсклусион</span><span class="sxs-lookup"><span data-stu-id="d2b15-103">ModuleExclusion Table</span></span>

<span data-ttu-id="d2b15-104">В таблице Модуликсклусион хранится список других модулей слияния, которые несовместимы в одной базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="d2b15-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="d2b15-105">Эта таблица включает средство слияния или проверки, чтобы убедиться в том, что конфликтующие модули слияния не объединяются в базе данных установщика пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2b15-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="d2b15-106">Средство проверяет, перекрестно ссылаясь на эту таблицу с помощью таблицы ModuleSignature в базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="d2b15-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="d2b15-107">Таблица Модуликсклусион содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d2b15-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="d2b15-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="d2b15-108">Column</span></span>             | <span data-ttu-id="d2b15-109">Type</span><span class="sxs-lookup"><span data-stu-id="d2b15-109">Type</span></span>                         | <span data-ttu-id="d2b15-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="d2b15-110">Key</span></span> | <span data-ttu-id="d2b15-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d2b15-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="d2b15-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="d2b15-112">ModuleID</span></span>           | [<span data-ttu-id="d2b15-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d2b15-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d2b15-114">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-114">Y</span></span>   | <span data-ttu-id="d2b15-115">Нет</span><span class="sxs-lookup"><span data-stu-id="d2b15-115">N</span></span>        |
| <span data-ttu-id="d2b15-116">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="d2b15-116">ModuleLanguage</span></span>     | [<span data-ttu-id="d2b15-117">Integer</span><span class="sxs-lookup"><span data-stu-id="d2b15-117">Integer</span></span>](integer.md)       | <span data-ttu-id="d2b15-118">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-118">Y</span></span>   | <span data-ttu-id="d2b15-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d2b15-119">N</span></span>        |
| <span data-ttu-id="d2b15-120">ексклудедид</span><span class="sxs-lookup"><span data-stu-id="d2b15-120">ExcludedID</span></span>         | [<span data-ttu-id="d2b15-121">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d2b15-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="d2b15-122">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-122">Y</span></span>   | <span data-ttu-id="d2b15-123">Нет</span><span class="sxs-lookup"><span data-stu-id="d2b15-123">N</span></span>        |
| <span data-ttu-id="d2b15-124">ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="d2b15-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="d2b15-125">Integer</span><span class="sxs-lookup"><span data-stu-id="d2b15-125">Integer</span></span>](integer.md)       | <span data-ttu-id="d2b15-126">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-126">Y</span></span>   | <span data-ttu-id="d2b15-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d2b15-127">N</span></span>        |
| <span data-ttu-id="d2b15-128">ексклудедминверсион</span><span class="sxs-lookup"><span data-stu-id="d2b15-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="d2b15-129">Version</span><span class="sxs-lookup"><span data-stu-id="d2b15-129">Version</span></span>](version.md)       |     | <span data-ttu-id="d2b15-130">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-130">Y</span></span>        |
| <span data-ttu-id="d2b15-131">ексклудедмаксверсион</span><span class="sxs-lookup"><span data-stu-id="d2b15-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="d2b15-132">Version</span><span class="sxs-lookup"><span data-stu-id="d2b15-132">Version</span></span>](version.md)       |     | <span data-ttu-id="d2b15-133">Да</span><span class="sxs-lookup"><span data-stu-id="d2b15-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d2b15-134">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d2b15-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d2b15-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="d2b15-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-136">Идентификатор модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="d2b15-136">Identifier of the merge module.</span></span> <span data-ttu-id="d2b15-137">Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2b15-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2b15-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="d2b15-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-139">Десятичный идентификатор языка модуля слияния в ModuleID.</span><span class="sxs-lookup"><span data-stu-id="d2b15-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="d2b15-140">Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2b15-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2b15-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ексклудедид</span><span class="sxs-lookup"><span data-stu-id="d2b15-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-142">Идентификатор исключенного модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="d2b15-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="d2b15-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="d2b15-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-144">Числовой идентификатор языка модуля слияния в Ексклудедид.</span><span class="sxs-lookup"><span data-stu-id="d2b15-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="d2b15-145">В столбце Ексклудедлангуаже можно указать идентификатор языка для одного языка, например 1033 для английского языка (США), или указать идентификатор языка для языковой группы, например 9 для любого английского языка.</span><span class="sxs-lookup"><span data-stu-id="d2b15-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="d2b15-146">Столбец Ексклудедлангуаже может принимать отрицательные идентификаторы языка.</span><span class="sxs-lookup"><span data-stu-id="d2b15-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="d2b15-147">Значение в столбце Ексклудедлангуаже выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d2b15-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="d2b15-148">ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="d2b15-148">ExcludedLanguage</span></span> | <span data-ttu-id="d2b15-149">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b15-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d2b15-150">> 0</span><span class="sxs-lookup"><span data-stu-id="d2b15-150">> 0</span></span>           | <span data-ttu-id="d2b15-151">Исключите идентификаторы языков, заданные параметром Ексклудедлангуаже.</span><span class="sxs-lookup"><span data-stu-id="d2b15-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="d2b15-152">= 0</span><span class="sxs-lookup"><span data-stu-id="d2b15-152">= 0</span></span>              | <span data-ttu-id="d2b15-153">Не исключать идентификаторы языков.</span><span class="sxs-lookup"><span data-stu-id="d2b15-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="d2b15-154">< 0</span><span class="sxs-lookup"><span data-stu-id="d2b15-154">< 0</span></span>           | <span data-ttu-id="d2b15-155">Исключите все идентификаторы языков, кроме тех, которые указаны параметром Ексклудедлангуаже.</span><span class="sxs-lookup"><span data-stu-id="d2b15-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d2b15-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ексклудедминверсион</span><span class="sxs-lookup"><span data-stu-id="d2b15-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-157">Минимальная версия, исключенная из диапазона.</span><span class="sxs-lookup"><span data-stu-id="d2b15-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="d2b15-158">Если поле Ексклудедминверсион имеет значение null, то все версии, предшествующие Ексклудедмаксверсион, исключаются.</span><span class="sxs-lookup"><span data-stu-id="d2b15-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="d2b15-159">Если оба Ексклудедминверсион и Ексклудедмаксверсион имеют значение null, нет исключений, основанных на версии.</span><span class="sxs-lookup"><span data-stu-id="d2b15-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="d2b15-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ексклудедмаксверсион</span><span class="sxs-lookup"><span data-stu-id="d2b15-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="d2b15-161">Максимальная версия, исключенная из диапазона.</span><span class="sxs-lookup"><span data-stu-id="d2b15-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="d2b15-162">Если поле Ексклудедмаксверсион имеет значение null, то все версии после Ексклудедминверсион исключаются.</span><span class="sxs-lookup"><span data-stu-id="d2b15-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="d2b15-163">Если оба Ексклудедминверсион и Ексклудедмаксверсион имеют значение null, нет исключений, основанных на версии.</span><span class="sxs-lookup"><span data-stu-id="d2b15-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d2b15-164">Проверка</span><span class="sxs-lookup"><span data-stu-id="d2b15-164">Validation</span></span>

<dl>

[<span data-ttu-id="d2b15-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="d2b15-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d2b15-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="d2b15-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d2b15-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="d2b15-167">ICE25</span></span>](ice25.md)  
</dl>

 

 




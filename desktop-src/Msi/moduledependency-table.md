---
description: В таблице Модуледепенденци хранится список других модулей слияния, необходимых для правильной работы этого модуля слияния.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Таблица Модуледепенденци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673939"
---
# <a name="moduledependency-table"></a><span data-ttu-id="76ed1-103">Таблица Модуледепенденци</span><span class="sxs-lookup"><span data-stu-id="76ed1-103">ModuleDependency Table</span></span>

<span data-ttu-id="76ed1-104">В таблице Модуледепенденци хранится список других модулей слияния, необходимых для правильной работы этого модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="76ed1-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="76ed1-105">Эта таблица включает средство слияния или проверки, чтобы убедиться в том, что необходимые модули слияния включены в базу данных установщика пользователя.</span><span class="sxs-lookup"><span data-stu-id="76ed1-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="76ed1-106">Средство проверяет, перекрестно ссылаясь на эту таблицу с помощью таблицы ModuleSignature в базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="76ed1-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="76ed1-107">Таблица Модуледепенденци содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="76ed1-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="76ed1-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="76ed1-108">Column</span></span>           | <span data-ttu-id="76ed1-109">Type</span><span class="sxs-lookup"><span data-stu-id="76ed1-109">Type</span></span>                         | <span data-ttu-id="76ed1-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="76ed1-110">Key</span></span> | <span data-ttu-id="76ed1-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="76ed1-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="76ed1-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="76ed1-112">ModuleID</span></span>         | [<span data-ttu-id="76ed1-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="76ed1-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="76ed1-114">Да</span><span class="sxs-lookup"><span data-stu-id="76ed1-114">Y</span></span>   | <span data-ttu-id="76ed1-115">Нет</span><span class="sxs-lookup"><span data-stu-id="76ed1-115">N</span></span>        |
| <span data-ttu-id="76ed1-116">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="76ed1-116">ModuleLanguage</span></span>   | [<span data-ttu-id="76ed1-117">Integer</span><span class="sxs-lookup"><span data-stu-id="76ed1-117">Integer</span></span>](integer.md)       | <span data-ttu-id="76ed1-118">Да</span><span class="sxs-lookup"><span data-stu-id="76ed1-118">Y</span></span>   | <span data-ttu-id="76ed1-119">Нет</span><span class="sxs-lookup"><span data-stu-id="76ed1-119">N</span></span>        |
| <span data-ttu-id="76ed1-120">рекуиредид</span><span class="sxs-lookup"><span data-stu-id="76ed1-120">RequiredID</span></span>       | [<span data-ttu-id="76ed1-121">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="76ed1-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="76ed1-122">Да</span><span class="sxs-lookup"><span data-stu-id="76ed1-122">Y</span></span>   | <span data-ttu-id="76ed1-123">Нет</span><span class="sxs-lookup"><span data-stu-id="76ed1-123">N</span></span>        |
| <span data-ttu-id="76ed1-124">рекуиредлангуаже</span><span class="sxs-lookup"><span data-stu-id="76ed1-124">RequiredLanguage</span></span> | [<span data-ttu-id="76ed1-125">Integer</span><span class="sxs-lookup"><span data-stu-id="76ed1-125">Integer</span></span>](integer.md)       | <span data-ttu-id="76ed1-126">Да</span><span class="sxs-lookup"><span data-stu-id="76ed1-126">Y</span></span>   | <span data-ttu-id="76ed1-127">Нет</span><span class="sxs-lookup"><span data-stu-id="76ed1-127">N</span></span>        |
| <span data-ttu-id="76ed1-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="76ed1-128">RequiredVersion</span></span>  | [<span data-ttu-id="76ed1-129">Version</span><span class="sxs-lookup"><span data-stu-id="76ed1-129">Version</span></span>](version.md)       |     | <span data-ttu-id="76ed1-130">Да</span><span class="sxs-lookup"><span data-stu-id="76ed1-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="76ed1-131">Столбцы</span><span class="sxs-lookup"><span data-stu-id="76ed1-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="76ed1-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="76ed1-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="76ed1-133">Идентификатор модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="76ed1-133">Identifier of the merge module.</span></span> <span data-ttu-id="76ed1-134">Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="76ed1-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ed1-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="76ed1-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="76ed1-136">Десятичный идентификатор языка модуля слияния в ModuleID.</span><span class="sxs-lookup"><span data-stu-id="76ed1-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="76ed1-137">Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="76ed1-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ed1-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>рекуиредид</span><span class="sxs-lookup"><span data-stu-id="76ed1-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="76ed1-139">Идентификатор модуля слияния, который требуется модулю слияния в ModuleID.</span><span class="sxs-lookup"><span data-stu-id="76ed1-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="76ed1-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>рекуиредлангуаже</span><span class="sxs-lookup"><span data-stu-id="76ed1-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="76ed1-141">Числовой идентификатор языка модуля слияния в Рекуиредид.</span><span class="sxs-lookup"><span data-stu-id="76ed1-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="76ed1-142">В столбце Рекуиредлангуаже можно указать идентификатор языка для одного языка, например 1033 для английского языка (США), или указать идентификатор языка для языковой группы, например 9 для любого английского языка.</span><span class="sxs-lookup"><span data-stu-id="76ed1-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="76ed1-143">Если поле содержит идентификатор языка группы, то любой модуль слияния с кодом языка в этой группе удовлетворяет зависимости.</span><span class="sxs-lookup"><span data-stu-id="76ed1-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="76ed1-144">Если Рекуиредлангуаже имеет значение 0, любой модуль слияния, заполняющий другие требования, удовлетворяет зависимости.</span><span class="sxs-lookup"><span data-stu-id="76ed1-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="76ed1-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="76ed1-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="76ed1-146">Версия модуля слияния в Рекуиредид.</span><span class="sxs-lookup"><span data-stu-id="76ed1-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="76ed1-147">Если это поле имеет значение null, любая версия заполняет зависимость.</span><span class="sxs-lookup"><span data-stu-id="76ed1-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="76ed1-148">Проверка</span><span class="sxs-lookup"><span data-stu-id="76ed1-148">Validation</span></span>

<dl>

[<span data-ttu-id="76ed1-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="76ed1-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="76ed1-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="76ed1-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="76ed1-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="76ed1-151">ICE25</span></span>](ice25.md)  
</dl>

 

 




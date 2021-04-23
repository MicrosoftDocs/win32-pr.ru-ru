---
description: Таблицу условий можно использовать для изменения состояния выбора любой записи в таблице компонентов на основе условного выражения.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Таблица условий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990926"
---
# <a name="condition-table"></a><span data-ttu-id="6493f-103">Таблица условий</span><span class="sxs-lookup"><span data-stu-id="6493f-103">Condition Table</span></span>

<span data-ttu-id="6493f-104">Таблицу условий можно использовать для изменения состояния выбора любой записи в [таблице компонентов](feature-table.md) на основе условного выражения.</span><span class="sxs-lookup"><span data-stu-id="6493f-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="6493f-105">Таблица условий содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="6493f-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="6493f-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="6493f-106">Column</span></span>    | <span data-ttu-id="6493f-107">Type</span><span class="sxs-lookup"><span data-stu-id="6493f-107">Type</span></span>                         | <span data-ttu-id="6493f-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="6493f-108">Key</span></span> | <span data-ttu-id="6493f-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="6493f-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="6493f-110">Функция\_</span><span class="sxs-lookup"><span data-stu-id="6493f-110">Feature\_</span></span> | [<span data-ttu-id="6493f-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6493f-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6493f-112">Да</span><span class="sxs-lookup"><span data-stu-id="6493f-112">Y</span></span>   | <span data-ttu-id="6493f-113">Нет</span><span class="sxs-lookup"><span data-stu-id="6493f-113">N</span></span>        |
| <span data-ttu-id="6493f-114">Level</span><span class="sxs-lookup"><span data-stu-id="6493f-114">Level</span></span>     | [<span data-ttu-id="6493f-115">Integer</span><span class="sxs-lookup"><span data-stu-id="6493f-115">Integer</span></span>](integer.md)       | <span data-ttu-id="6493f-116">Да</span><span class="sxs-lookup"><span data-stu-id="6493f-116">Y</span></span>   | <span data-ttu-id="6493f-117">Нет</span><span class="sxs-lookup"><span data-stu-id="6493f-117">N</span></span>        |
| <span data-ttu-id="6493f-118">Условие</span><span class="sxs-lookup"><span data-stu-id="6493f-118">Condition</span></span> | [<span data-ttu-id="6493f-119">Condition</span><span class="sxs-lookup"><span data-stu-id="6493f-119">Condition</span></span>](condition.md)   | <span data-ttu-id="6493f-120">Нет</span><span class="sxs-lookup"><span data-stu-id="6493f-120">N</span></span>   | <span data-ttu-id="6493f-121">Да</span><span class="sxs-lookup"><span data-stu-id="6493f-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6493f-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="6493f-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6493f-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="6493f-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="6493f-124">Внешний ключ в столбце одна из таблиц Feature.</span><span class="sxs-lookup"><span data-stu-id="6493f-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="6493f-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Уровню</span><span class="sxs-lookup"><span data-stu-id="6493f-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="6493f-126">Условный уровень установки для функции в столбце "компонент" \_ этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="6493f-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="6493f-127">Установщик устанавливает уровень установки этой функции на уровень, указанный в этом столбце, если выражение в столбце Condition имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="6493f-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="6493f-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Выполняет</span><span class="sxs-lookup"><span data-stu-id="6493f-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="6493f-129">Если условное выражение принимает значение TRUE, то столбец Level в таблице Feature устанавливается на уровень условной установки.</span><span class="sxs-lookup"><span data-stu-id="6493f-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="6493f-130">Выражение в столбце Condition не должно содержать ссылки на установленное состояние любого компонента или компонента.</span><span class="sxs-lookup"><span data-stu-id="6493f-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="6493f-131">Это обусловлено тем, что выражения в столбце Условие оцениваются до того, как установщик оценивает установленные состояния компонентов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="6493f-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="6493f-132">Любое выражение в таблице условие, которое пытается проверить установленное состояние компонента или компонента, всегда имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="6493f-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="6493f-133">Дополнительные сведения о синтаксисе условных операторов см. в разделе [Синтаксис условных](conditional-statement-syntax.md)инструкций.</span><span class="sxs-lookup"><span data-stu-id="6493f-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6493f-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6493f-134">Remarks</span></span>

<span data-ttu-id="6493f-135">Компонент можно навсегда отключить, установив для столбца Level значение 0.</span><span class="sxs-lookup"><span data-stu-id="6493f-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="6493f-136">Уровень может быть установлен на основе любой условной инструкции, такой как тест для платформы, операционной системы или определенного значения свойства.</span><span class="sxs-lookup"><span data-stu-id="6493f-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="6493f-137">Следует тщательно выбрать условия, чтобы функция не была включена при установке, а затем была отключена при удалении.</span><span class="sxs-lookup"><span data-stu-id="6493f-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="6493f-138">Эта функция будет утеряна, и продукт не будет удален.</span><span class="sxs-lookup"><span data-stu-id="6493f-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="6493f-139">Эта таблица упоминается при выполнении [действия костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="6493f-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="6493f-140">Если предварительно [**выбранное**](preselected.md) свойство было установлено в 1, установщик не оценивает таблицу условий.</span><span class="sxs-lookup"><span data-stu-id="6493f-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="6493f-141">Таблица условий влияет только на установку компонентов, если не задано ни одно из следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="6493f-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="6493f-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="6493f-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="6493f-143">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="6493f-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="6493f-144">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="6493f-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="6493f-145">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="6493f-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="6493f-146">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="6493f-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="6493f-147">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="6493f-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="6493f-148">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="6493f-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="6493f-149">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="6493f-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="6493f-150">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="6493f-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="6493f-151">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="6493f-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="6493f-152">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="6493f-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="6493f-153">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="6493f-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="6493f-154">Проверка</span><span class="sxs-lookup"><span data-stu-id="6493f-154">Validation</span></span>

<dl>

[<span data-ttu-id="6493f-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="6493f-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6493f-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="6493f-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6493f-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="6493f-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="6493f-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="6493f-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="6493f-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="6493f-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="6493f-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="6493f-160">ICE86</span></span>](ice86.md)  
</dl>

 

 




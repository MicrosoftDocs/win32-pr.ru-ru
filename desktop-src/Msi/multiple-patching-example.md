---
description: В следующем примере показано, как установщик Windows 3,0 и более поздних версий можно использовать для применения исправлений в том порядке, в котором они созданы.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Пример с несколькими исправлениями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673563"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="40a0e-103">Пример с несколькими исправлениями</span><span class="sxs-lookup"><span data-stu-id="40a0e-103">Multiple Patching Example</span></span>

<span data-ttu-id="40a0e-104">В следующем примере показано, как установщик Windows 3,0 и более поздних версий можно использовать для применения исправлений в том порядке, в котором они созданы.</span><span class="sxs-lookup"><span data-stu-id="40a0e-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="40a0e-105">Пример</span><span class="sxs-lookup"><span data-stu-id="40a0e-105">Example</span></span>

<span data-ttu-id="40a0e-106">В этом примере есть три исправления: QFE1, QFE2 и ServicePack1, и у каждого из них есть таблица [мсипатчсекуенце](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="40a0e-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="40a0e-107">Эти исправления были созданы для применения к версии 1,0 приложения.</span><span class="sxs-lookup"><span data-stu-id="40a0e-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="40a0e-108">Имя исправления</span><span class="sxs-lookup"><span data-stu-id="40a0e-108">Patch Name</span></span>   | <span data-ttu-id="40a0e-109">Тип исправления</span><span class="sxs-lookup"><span data-stu-id="40a0e-109">Patch Type</span></span>    | <span data-ttu-id="40a0e-110">Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="40a0e-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="40a0e-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="40a0e-111">QFE1</span></span>         | <span data-ttu-id="40a0e-112">Небольшое обновление</span><span class="sxs-lookup"><span data-stu-id="40a0e-112">Small Update</span></span>  | <span data-ttu-id="40a0e-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-113">1.1.0</span></span>           |
| <span data-ttu-id="40a0e-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="40a0e-114">QFE2</span></span>         | <span data-ttu-id="40a0e-115">Небольшое обновление</span><span class="sxs-lookup"><span data-stu-id="40a0e-115">Small Update</span></span>  | <span data-ttu-id="40a0e-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-116">1.2.0</span></span>           |
| <span data-ttu-id="40a0e-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="40a0e-117">ServicePack1</span></span> | <span data-ttu-id="40a0e-118">Незначительное обновление</span><span class="sxs-lookup"><span data-stu-id="40a0e-118">Minor Upgrade</span></span> | <span data-ttu-id="40a0e-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-119">1.3.0</span></span>           |



 

<span data-ttu-id="40a0e-120">Таблица [мсипатчсекуенце](msipatchsequence-table.md) каждого исправления содержит только одну запись, содержащую семейство исправлений, код продукта и порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="40a0e-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="40a0e-121">Все три исправления применяются к одному и тому же продукту и принадлежат одному семейству исправлений с именем Апппатч.</span><span class="sxs-lookup"><span data-stu-id="40a0e-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="40a0e-122">Ни один из исправлений не имеет атрибута **мсидбпатчсекуенцесуперседиарлиер** .</span><span class="sxs-lookup"><span data-stu-id="40a0e-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="40a0e-123">[Таблица мсипатчсекуенце](msipatchsequence-table.md) для QFE1 [малого обновления](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="40a0e-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="40a0e-124">патчфамили</span><span class="sxs-lookup"><span data-stu-id="40a0e-124">PatchFamily</span></span> | <span data-ttu-id="40a0e-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="40a0e-125">ProductCode</span></span>                            | <span data-ttu-id="40a0e-126">Последовательность</span><span class="sxs-lookup"><span data-stu-id="40a0e-126">Sequence</span></span> | <span data-ttu-id="40a0e-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="40a0e-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="40a0e-128">апппатч</span><span class="sxs-lookup"><span data-stu-id="40a0e-128">AppPatch</span></span>    | <span data-ttu-id="40a0e-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="40a0e-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="40a0e-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="40a0e-131">[Таблица мсипатчсекуенце](msipatchsequence-table.md) для QFE2 [малого обновления](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="40a0e-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="40a0e-132">патчфамили</span><span class="sxs-lookup"><span data-stu-id="40a0e-132">PatchFamily</span></span> | <span data-ttu-id="40a0e-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="40a0e-133">ProductCode</span></span>                            | <span data-ttu-id="40a0e-134">Последовательность</span><span class="sxs-lookup"><span data-stu-id="40a0e-134">Sequence</span></span> | <span data-ttu-id="40a0e-135">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="40a0e-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="40a0e-136">апппатч</span><span class="sxs-lookup"><span data-stu-id="40a0e-136">AppPatch</span></span>    | <span data-ttu-id="40a0e-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="40a0e-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="40a0e-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="40a0e-139">[Таблица мсипатчсекуенце](msipatchsequence-table.md) для [незначительного обновления](minor-upgrades.md)ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="40a0e-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="40a0e-140">патчфамили</span><span class="sxs-lookup"><span data-stu-id="40a0e-140">PatchFamily</span></span> | <span data-ttu-id="40a0e-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="40a0e-141">ProductCode</span></span>                            | <span data-ttu-id="40a0e-142">Последовательность</span><span class="sxs-lookup"><span data-stu-id="40a0e-142">Sequence</span></span> | <span data-ttu-id="40a0e-143">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="40a0e-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="40a0e-144">апппатч</span><span class="sxs-lookup"><span data-stu-id="40a0e-144">AppPatch</span></span>    | <span data-ttu-id="40a0e-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="40a0e-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="40a0e-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="40a0e-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="40a0e-147">Если пользователь устанавливает версию 1,0 продукта, а затем применяет QFE2, а затем в дальнейшем решает применить QFE1, установщик Windows гарантирует, что эффективная последовательность применения исправлений к продукту QFE1 будет применена перед QFE2.</span><span class="sxs-lookup"><span data-stu-id="40a0e-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="40a0e-148">Если пользователь применяет ServicePack1, применяет QFE2 и QFE1 вместе в более поздней версии, установщик Windows гарантирует, что эффективная последовательность приложения исправления будет QFE1 впереди QFE2 и впереди ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="40a0e-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="40a0e-149">Если ServicePack1 **мсидбпатчсекуенцесуперседиарлиер** задан в столбце Attributes таблицы [мсипатчсекуенце](msipatchsequence-table.md) , это означает, что пакет обновления содержит все изменения в QFE1 и QFE2.</span><span class="sxs-lookup"><span data-stu-id="40a0e-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="40a0e-150">В этом случае QFE1 и QFE2 не применяются при применении ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="40a0e-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="40a0e-151">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40a0e-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="40a0e-152">Версии, предшествующие установщик Windows 3,0, могут устанавливать только одно исправление для каждой транзакции, а исправления применяются в той последовательности, в которой они указаны.</span><span class="sxs-lookup"><span data-stu-id="40a0e-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="40a0e-153">В предыдущем примере, если сначала применяется QFE2, а затем применяется QFE1, то это две транзакции, а исправления применяются к версии 1,0 приложения в последовательности QFE2, за которой следует QFE1.</span><span class="sxs-lookup"><span data-stu-id="40a0e-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="40a0e-154">Если сначала применяется ServicePack1, то QFE1 или QFE2 нельзя применить в более поздней транзакции, так как ServicePack1 является незначительным обновлением, которое изменяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="40a0e-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="40a0e-155">QFE1 и QFE2 можно применять только к версии 1,0 приложения.</span><span class="sxs-lookup"><span data-stu-id="40a0e-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 




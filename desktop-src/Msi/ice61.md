---
description: ICE61 проверяет таблицу обновления установщик Windows базы данных.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650975"
---
# <a name="ice61"></a><span data-ttu-id="ab015-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="ab015-103">ICE61</span></span>

<span data-ttu-id="ab015-104">ICE61 проверяет таблицу обновления, чтобы убедиться в соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="ab015-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="ab015-105">Все свойства Актионпроперти не были предварительно созданы в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="ab015-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="ab015-106">Все свойства Актионпроперти являются общими свойствами.</span><span class="sxs-lookup"><span data-stu-id="ab015-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="ab015-107">Все свойства Актионпроперти включены в свойство [**секурекустомпропертиес**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="ab015-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="ab015-108">Все свойства Актионпроперти уникальны для каждой записи в таблице обновления.</span><span class="sxs-lookup"><span data-stu-id="ab015-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="ab015-109">Все значения Версионмакс не меньше соответствующих значений Версионмин.</span><span class="sxs-lookup"><span data-stu-id="ab015-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="ab015-110">Значения Версионмин и Версионмакс являются допустимыми версиями продукта.</span><span class="sxs-lookup"><span data-stu-id="ab015-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="ab015-111">Допустимый формат версии продукта см. в свойстве [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="ab015-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="ab015-112">Попытка удалить более новую или равную версию текущего продукта не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab015-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="ab015-113">Ошибка исправления предупреждения или ошибки, о которой сообщает ICE61, обычно приводит к проблемам при обновлении приложения.</span><span class="sxs-lookup"><span data-stu-id="ab015-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="ab015-114">В зависимости от точной ошибки это может быть любая из файлов из более старой версии, удаление файлов из старой версии, несмотря на то, что они необходимы для нового приложения, или завершении сбоя обновления.</span><span class="sxs-lookup"><span data-stu-id="ab015-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="ab015-115">Результат</span><span class="sxs-lookup"><span data-stu-id="ab015-115">Result</span></span>

<span data-ttu-id="ab015-116">ICE61 отправляет предупреждение или ошибку, если любое из указанных выше условий имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ab015-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="ab015-117">Пример</span><span class="sxs-lookup"><span data-stu-id="ab015-117">Example</span></span>

<span data-ttu-id="ab015-118">ICE61 сообщает о следующих ошибках и предупреждении для приведенных примеров.</span><span class="sxs-lookup"><span data-stu-id="ab015-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="ab015-119">В этом случае в первой строке будет предпринята попытка удалить продукт той же версии.</span><span class="sxs-lookup"><span data-stu-id="ab015-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="ab015-120">(Столбец Версионмакс равен версии продукта в таблице свойств).</span><span class="sxs-lookup"><span data-stu-id="ab015-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="ab015-121">Чтобы устранить эту ошибку, используйте версию в столбце Версионмакс ниже, чем текущая версия, указанная в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="ab015-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="ab015-122">Удалите бит **мсидбупградеаттрибутесверсионмаксинклусиве** из столбца Attributes, если значение версионмакс равно текущей версии.</span><span class="sxs-lookup"><span data-stu-id="ab015-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="ab015-123">Если намерение обнаруживает только продукт и не удаляет его, добавление бита **мсидбупградеаттрибутесонлидетект** к столбцу Attributes также приведет к устранению этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="ab015-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="ab015-124">Если свойство не указано в свойстве [**секурекустомпропертиес**](securecustomproperties.md) , оно не передается на серверную часть установки при обнаружении свойства.</span><span class="sxs-lookup"><span data-stu-id="ab015-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="ab015-125">Чтобы устранить эту ошибку, добавьте свойство в [**секурекустомпропертиес**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="ab015-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="ab015-126">Свойства обновления должны быть общедоступными свойствами для передачи результата на серверную часть установки.</span><span class="sxs-lookup"><span data-stu-id="ab015-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="ab015-127">Чтобы устранить эту ошибку, используйте все прописные буквы в имени свойства.</span><span class="sxs-lookup"><span data-stu-id="ab015-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="ab015-128">Свойство может использоваться только в одной строке таблицы обновления.</span><span class="sxs-lookup"><span data-stu-id="ab015-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="ab015-129">Чтобы устранить эту ошибку, используйте другое свойство для второй строки.</span><span class="sxs-lookup"><span data-stu-id="ab015-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="ab015-130">Минимальная версия должна быть меньше максимальной версии.</span><span class="sxs-lookup"><span data-stu-id="ab015-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="ab015-131">Чтобы устранить эту ошибку, проверьте номера версий на наличие опечаток.</span><span class="sxs-lookup"><span data-stu-id="ab015-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="ab015-132">Если они верны и вы хотите использовать диапазон между двумя версиями, переключите их так, чтобы Версионмин меньше Версионмакс.</span><span class="sxs-lookup"><span data-stu-id="ab015-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="ab015-133">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="ab015-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="ab015-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="ab015-134">Property</span></span>                                                 | <span data-ttu-id="ab015-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ab015-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="ab015-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ab015-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="ab015-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="ab015-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="ab015-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="ab015-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="ab015-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="ab015-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="ab015-140">**секурекустомпропертиес**</span><span class="sxs-lookup"><span data-stu-id="ab015-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="ab015-141">олдаппфаунд</span><span class="sxs-lookup"><span data-stu-id="ab015-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="ab015-142">Обновление таблицы</span><span class="sxs-lookup"><span data-stu-id="ab015-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="ab015-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="ab015-143">UpgradeCode</span></span>                            | <span data-ttu-id="ab015-144">версионмин</span><span class="sxs-lookup"><span data-stu-id="ab015-144">VersionMin</span></span> | <span data-ttu-id="ab015-145">версионмакс</span><span class="sxs-lookup"><span data-stu-id="ab015-145">VersionMax</span></span> | <span data-ttu-id="ab015-146">Язык</span><span class="sxs-lookup"><span data-stu-id="ab015-146">Language</span></span> | <span data-ttu-id="ab015-147">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ab015-147">Attributes</span></span> | <span data-ttu-id="ab015-148">Удалить</span><span class="sxs-lookup"><span data-stu-id="ab015-148">Remove</span></span>                | <span data-ttu-id="ab015-149">актионпроперти</span><span class="sxs-lookup"><span data-stu-id="ab015-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="ab015-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="ab015-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="ab015-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="ab015-151">2.01.0000</span></span>  |          | <span data-ttu-id="ab015-152">513</span><span class="sxs-lookup"><span data-stu-id="ab015-152">513</span></span>        |                       | <span data-ttu-id="ab015-153">олдаппфаунд</span><span class="sxs-lookup"><span data-stu-id="ab015-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="ab015-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="ab015-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="ab015-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="ab015-155">2.01.0001</span></span>  | <span data-ttu-id="ab015-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="ab015-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="ab015-157">олдаппфаунд</span><span class="sxs-lookup"><span data-stu-id="ab015-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="ab015-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="ab015-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="ab015-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="ab015-159">1.00.0000</span></span>  | <span data-ttu-id="ab015-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="ab015-160">2.00.0000</span></span>  | <span data-ttu-id="ab015-161">1033</span><span class="sxs-lookup"><span data-stu-id="ab015-161">1033</span></span>     |            | <span data-ttu-id="ab015-162">\[аппфеатуринглиш\]</span><span class="sxs-lookup"><span data-stu-id="ab015-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="ab015-163">енглишаппфаунд</span><span class="sxs-lookup"><span data-stu-id="ab015-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ab015-164">См. также</span><span class="sxs-lookup"><span data-stu-id="ab015-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab015-165">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="ab015-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




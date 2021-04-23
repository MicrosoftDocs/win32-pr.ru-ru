---
description: ICE30 проверяет, что установка компонентов, содержащих один и тот же файл, никогда не устанавливала файл более одного раза в одном каталоге.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663664"
---
# <a name="ice30"></a><span data-ttu-id="a9a2f-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="a9a2f-103">ICE30</span></span>

<span data-ttu-id="a9a2f-104">ICE30 проверяет, что установка компонентов, содержащих один и тот же файл, никогда не устанавливала файл более одного раза в одном каталоге.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="a9a2f-105">ICE30 переходит к каждому компоненту в [таблице Component](component-table.md) , а затем определяет целевой каталог компонента из [таблицы Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="a9a2f-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="a9a2f-106">Затем он проверяет, какие из этих компонентов устанавливаются в один и тот же целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="a9a2f-107">Наконец, он использует [таблицу File](file-table.md) для проверки того, что ни один из файлов в этих компонентах не имеет такого же имени.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="a9a2f-108">ICE30 проверяет длинные имена файлов (ЛФН) и короткие имена файлов (СФН).</span><span class="sxs-lookup"><span data-stu-id="a9a2f-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="a9a2f-109">ICE30 не вычисляет свойства в разрешении каталогов, так как эти свойства могут изменяться во время выполнения и изменять схему разрешения каталогов.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="a9a2f-110">Это означает, что ICE30 может обнаруживать конфликты файлов из-за наличия каталогов с тем же свойством в путях, но не обнаруживает конфликты, вызванные двумя свойствами с одинаковым значением.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="a9a2f-111">Результат</span><span class="sxs-lookup"><span data-stu-id="a9a2f-111">Result</span></span>

<span data-ttu-id="a9a2f-112">ICE30 отправляет сообщение об ошибке для каждой пары компонентов, которая устанавливает один и тот же файл в тот же каталог.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="a9a2f-113">Пример</span><span class="sxs-lookup"><span data-stu-id="a9a2f-113">Example</span></span>

<span data-ttu-id="a9a2f-114">Приведенный пример возвращает два следующих ошибки дважды.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="a9a2f-115">Ошибка или предупреждение ICE30</span><span class="sxs-lookup"><span data-stu-id="a9a2f-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="a9a2f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a9a2f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a2f-117">Ошибка: целевой файл README. 1st установлен в "TARGETDIR \\ Product" двумя различными компонентами в системе СФН: "Component1" и "Component2".</span><span class="sxs-lookup"><span data-stu-id="a9a2f-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="a9a2f-118">Это приводит к разрыву подсчета ссылок на компоненты.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="a9a2f-119">Component1 и Component2 имеют файл с именем "РЕАДЕМЕ. 1st".</span><span class="sxs-lookup"><span data-stu-id="a9a2f-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="a9a2f-120">При использовании коротких имен файлов установщик устанавливает Dir1 и Dir2 в один каталог, TARGETDIR \\ Product.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="a9a2f-121">ICE30 создает две ошибки — по одной для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="a9a2f-122">В среде разработки, отображающей расположения ошибок, первая ошибка находится в записи файла в [таблице File](file-table.md), а вторая — в расположении другого файла.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="a9a2f-123">ОШИБКА. Установка условного компонента приведет к установке целевого файла README. 1st в " \\ Общие средства TARGETDIR" двумя разными компонентами в системе лфн: "Component3" и "Component4".</span><span class="sxs-lookup"><span data-stu-id="a9a2f-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="a9a2f-124">Это приведет к нарушению подсчета ссылок на компоненты.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="a9a2f-125">Component4 содержит запись в столбце Condition [таблицы Component](component-table.md) , а Component3 — нет.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="a9a2f-126">Если [**версионнт**](versionnt.md) имеет значение true, устанавливается Component4 и возникает конфликт с файлом readme. первый всегда установлен с помощью Component3.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="a9a2f-127">ICE30 создает 4 ошибки, одну пару для СФН, одну для ЛФН.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="a9a2f-128">ВНИМАНИЕ! целевой файл "README. 1st" может быть установлен в " \\ Общие средства TARGETDIR" двумя различными условными компонентами в системе СФН: "Component4" и "Component5".</span><span class="sxs-lookup"><span data-stu-id="a9a2f-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="a9a2f-129">Если условия не являются взаимоисключающими, это приведет к нарушению системы подсчета ссылок на компоненты.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="a9a2f-130">Так как Component4 и Component5 содержат записи в столбце Condition [таблицы Component](component-table.md) , этот конфликт файлов может не произойти.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="a9a2f-131">ICE30 отправляет только предупреждение, так как условия должны быть определены во время установки.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="a9a2f-132">ICE30 создает 4 предупреждения, одну пару для СФН, одну для ЛФН.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="a9a2f-133">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a9a2f-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a9a2f-134">Компонент</span><span class="sxs-lookup"><span data-stu-id="a9a2f-134">Component</span></span>  | <span data-ttu-id="a9a2f-135">Каталог</span><span class="sxs-lookup"><span data-stu-id="a9a2f-135">Directory</span></span> | <span data-ttu-id="a9a2f-136">Условие</span><span class="sxs-lookup"><span data-stu-id="a9a2f-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="a9a2f-137">Component1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-137">Component1</span></span> | <span data-ttu-id="a9a2f-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-138">Dir1</span></span>      |           |
| <span data-ttu-id="a9a2f-139">Component2</span><span class="sxs-lookup"><span data-stu-id="a9a2f-139">Component2</span></span> | <span data-ttu-id="a9a2f-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="a9a2f-140">Dir2</span></span>      |           |
| <span data-ttu-id="a9a2f-141">Component3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-141">Component3</span></span> | <span data-ttu-id="a9a2f-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-142">Dir3</span></span>      |           |
| <span data-ttu-id="a9a2f-143">Component4</span><span class="sxs-lookup"><span data-stu-id="a9a2f-143">Component4</span></span> | <span data-ttu-id="a9a2f-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-144">Dir3</span></span>      | <span data-ttu-id="a9a2f-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="a9a2f-145">VersionNT</span></span> |
| <span data-ttu-id="a9a2f-146">Component5</span><span class="sxs-lookup"><span data-stu-id="a9a2f-146">Component5</span></span> | <span data-ttu-id="a9a2f-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-147">Dir3</span></span>      | <span data-ttu-id="a9a2f-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="a9a2f-148">Version9X</span></span> |



 

[<span data-ttu-id="a9a2f-149">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="a9a2f-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="a9a2f-150">Каталог</span><span class="sxs-lookup"><span data-stu-id="a9a2f-150">Directory</span></span> | <span data-ttu-id="a9a2f-151">Родительский \_ Каталог</span><span class="sxs-lookup"><span data-stu-id="a9a2f-151">Parent\_Directory</span></span> | <span data-ttu-id="a9a2f-152">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="a9a2f-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="a9a2f-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="a9a2f-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="a9a2f-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-155">Dir1</span></span>      | <span data-ttu-id="a9a2f-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-156">SOURCEDIR</span></span>         | <span data-ttu-id="a9a2f-157">\|Продукт Component1 продукта:.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="a9a2f-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="a9a2f-158">Dir2</span></span>      | <span data-ttu-id="a9a2f-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-159">SOURCEDIR</span></span>         | <span data-ttu-id="a9a2f-160">Продукт:.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-160">Product:.</span></span>                     |
| <span data-ttu-id="a9a2f-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-161">Dir3</span></span>      | <span data-ttu-id="a9a2f-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-162">SOURCEDIR</span></span>         | <span data-ttu-id="a9a2f-163">Распространенные \| Общие средства:</span><span class="sxs-lookup"><span data-stu-id="a9a2f-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="a9a2f-164">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="a9a2f-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a9a2f-165">Файл</span><span class="sxs-lookup"><span data-stu-id="a9a2f-165">File</span></span>  | <span data-ttu-id="a9a2f-166">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a9a2f-166">Component\_</span></span> | <span data-ttu-id="a9a2f-167">FileName</span><span class="sxs-lookup"><span data-stu-id="a9a2f-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="a9a2f-168">Файл1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-168">File1</span></span> | <span data-ttu-id="a9a2f-169">Component1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-169">Component1</span></span>  | <span data-ttu-id="a9a2f-170">ФАЙЛ README. 1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-170">README.1st</span></span> |
| <span data-ttu-id="a9a2f-171">Файл2</span><span class="sxs-lookup"><span data-stu-id="a9a2f-171">File2</span></span> | <span data-ttu-id="a9a2f-172">Component2</span><span class="sxs-lookup"><span data-stu-id="a9a2f-172">Component2</span></span>  | <span data-ttu-id="a9a2f-173">ФАЙЛ README. 1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-173">README.1st</span></span> |
| <span data-ttu-id="a9a2f-174">Файл3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-174">File3</span></span> | <span data-ttu-id="a9a2f-175">Component3</span><span class="sxs-lookup"><span data-stu-id="a9a2f-175">Component3</span></span>  | <span data-ttu-id="a9a2f-176">ФАЙЛ README. 1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-176">README.1st</span></span> |
| <span data-ttu-id="a9a2f-177">Файл4</span><span class="sxs-lookup"><span data-stu-id="a9a2f-177">File4</span></span> | <span data-ttu-id="a9a2f-178">Component4</span><span class="sxs-lookup"><span data-stu-id="a9a2f-178">Component4</span></span>  | <span data-ttu-id="a9a2f-179">ФАЙЛ README. 1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-179">README.1st</span></span> |
| <span data-ttu-id="a9a2f-180">Файл5</span><span class="sxs-lookup"><span data-stu-id="a9a2f-180">File5</span></span> | <span data-ttu-id="a9a2f-181">Component5</span><span class="sxs-lookup"><span data-stu-id="a9a2f-181">Component5</span></span>  | <span data-ttu-id="a9a2f-182">ФАЙЛ README. 1</span><span class="sxs-lookup"><span data-stu-id="a9a2f-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9a2f-183">См. также</span><span class="sxs-lookup"><span data-stu-id="a9a2f-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a2f-184">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="a9a2f-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 





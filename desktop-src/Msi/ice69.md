---
description: ICE69 проверяет, что все подстроки формы \[ $componentkey \] в отформатированной строке не имеют перекрестных ссылок на компоненты.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266133"
---
# <a name="ice69"></a><span data-ttu-id="126ca-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="126ca-103">ICE69</span></span>

<span data-ttu-id="126ca-104">ICE69 проверяет, что все подстроки формы \[ $componentkey \] в [отформатированной](formatted.md) строке не имеют перекрестных ссылок на компоненты.</span><span class="sxs-lookup"><span data-stu-id="126ca-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="126ca-105">Ссылка на кросс-компоненты возникает, когда \[ \] свойство $componentkey форматированной строки ссылается на компонент, отличный от компонента, хранящегося в столбце Component \_ таблиц.</span><span class="sxs-lookup"><span data-stu-id="126ca-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="126ca-106">Проблемы с ссылками между компонентами возникают из-за того, как [отформатированные](formatted.md) строки вычисляются.</span><span class="sxs-lookup"><span data-stu-id="126ca-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="126ca-107">Если компонент, на который ссылается \[ свойство $componentkey, \] уже установлен и не изменяется во время текущей установки (например, переустановка, перемещение в источник и т. д.), выражение \[ $componentkey \] вычисляется как null, так как состояние действия компонента в \[ $componentkey \] равно null.</span><span class="sxs-lookup"><span data-stu-id="126ca-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="126ca-108">Аналогичные проблемы могут возникнуть во время операций обновления и восстановления.</span><span class="sxs-lookup"><span data-stu-id="126ca-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="126ca-109">Результат</span><span class="sxs-lookup"><span data-stu-id="126ca-109">Result</span></span>

<span data-ttu-id="126ca-110">ICE69 возвращает ошибку, если \[ $componentkey \] подстрока в [отформатированной](formatted.md) строке перекрестно ссылается на компонент в другой функции.</span><span class="sxs-lookup"><span data-stu-id="126ca-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="126ca-111">ICE69 возвращает предупреждение, $componentkey если \[ \] подстрока в отформатированной строке перекрестно ссылается на компонент в той же функции.</span><span class="sxs-lookup"><span data-stu-id="126ca-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="126ca-112">(Для определения этого сопоставления используется таблица [феатурекомпонентс](featurecomponents-table.md) .</span><span class="sxs-lookup"><span data-stu-id="126ca-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="126ca-113">Он должен соответствовать той же функции для предупреждения.</span><span class="sxs-lookup"><span data-stu-id="126ca-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="126ca-114">Создание ссылок на компоненты в родительских компонентах или на ссылки на компоненты в дочерних функциях считается ошибкой.)</span><span class="sxs-lookup"><span data-stu-id="126ca-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="126ca-115">ICE69 сообщает об ошибке, если \[ \# \] подстрока филекэй в [форматированной](formatted.md) строке ссылается на файл, который не указан в таблице [File](file-table.md) как принадлежащий тому же компоненту.</span><span class="sxs-lookup"><span data-stu-id="126ca-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="126ca-116">Пример</span><span class="sxs-lookup"><span data-stu-id="126ca-116">Example</span></span>

<span data-ttu-id="126ca-117">ICE69 сообщает о следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="126ca-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="126ca-118">Чтобы устранить эту ошибку, не следует выполнять перекрестные ссылки на компоненты.</span><span class="sxs-lookup"><span data-stu-id="126ca-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="126ca-119">Измените \[ $componentkey \] в соответствии с компонентом ярлыка.</span><span class="sxs-lookup"><span data-stu-id="126ca-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="126ca-120">[Таблица ярлыков](shortcut-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="126ca-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="126ca-121">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="126ca-121">Shortcut</span></span>  | <span data-ttu-id="126ca-122">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="126ca-122">Component\_</span></span> | <span data-ttu-id="126ca-123">Аргумент</span><span class="sxs-lookup"><span data-stu-id="126ca-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="126ca-124">Тест</span><span class="sxs-lookup"><span data-stu-id="126ca-124">Test</span></span>      | <span data-ttu-id="126ca-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="126ca-125">QuickTest</span></span>   | <span data-ttu-id="126ca-126">-v \[ $Test\]</span><span class="sxs-lookup"><span data-stu-id="126ca-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="126ca-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="126ca-127">Shortcut2</span></span> | <span data-ttu-id="126ca-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="126ca-128">QuickTest</span></span>   | <span data-ttu-id="126ca-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="126ca-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="126ca-130">Таблицы [команд](verb-table.md) и [расширений](extension-table.md) — это особые случаи, в которых таблица команд ссылается на расширение, которое принадлежит компоненту.</span><span class="sxs-lookup"><span data-stu-id="126ca-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="126ca-131">Однако расширение может принадлежать нескольким компонентам, так как первичный ключ для таблицы расширений состоит из столбцов расширения и компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="126ca-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="126ca-132">Вы можете логически использовать следующую ситуацию.</span><span class="sxs-lookup"><span data-stu-id="126ca-132">You can logically have the following situation.</span></span>

<span data-ttu-id="126ca-133">[Таблица команд](verb-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="126ca-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="126ca-134">Расширение</span><span class="sxs-lookup"><span data-stu-id="126ca-134">Extension</span></span> | <span data-ttu-id="126ca-135">Команда\_</span><span class="sxs-lookup"><span data-stu-id="126ca-135">Verb\_</span></span> | <span data-ttu-id="126ca-136">Аргумент</span><span class="sxs-lookup"><span data-stu-id="126ca-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="126ca-137">TST</span><span class="sxs-lookup"><span data-stu-id="126ca-137">tst</span></span>       | <span data-ttu-id="126ca-138">open</span><span class="sxs-lookup"><span data-stu-id="126ca-138">open</span></span>   | <span data-ttu-id="126ca-139">-v \[ $comp 1 \] \[ $comp 2\]</span><span class="sxs-lookup"><span data-stu-id="126ca-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="126ca-140">[Таблица расширения](extension-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="126ca-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="126ca-141">Расширение</span><span class="sxs-lookup"><span data-stu-id="126ca-141">Extension</span></span> | <span data-ttu-id="126ca-142">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="126ca-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="126ca-143">TST</span><span class="sxs-lookup"><span data-stu-id="126ca-143">tst</span></span>       | <span data-ttu-id="126ca-144">comp1</span><span class="sxs-lookup"><span data-stu-id="126ca-144">comp1</span></span>       |
| <span data-ttu-id="126ca-145">TST</span><span class="sxs-lookup"><span data-stu-id="126ca-145">tst</span></span>       | <span data-ttu-id="126ca-146">Comp2</span><span class="sxs-lookup"><span data-stu-id="126ca-146">comp2</span></span>       |



 

[<span data-ttu-id="126ca-147">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="126ca-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="126ca-148">Функция\_</span><span class="sxs-lookup"><span data-stu-id="126ca-148">Feature\_</span></span> | <span data-ttu-id="126ca-149">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="126ca-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="126ca-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="126ca-150">Feature1</span></span>  | <span data-ttu-id="126ca-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="126ca-151">QuickTest</span></span>   |
| <span data-ttu-id="126ca-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="126ca-152">Feature1</span></span>  | <span data-ttu-id="126ca-153">Тест</span><span class="sxs-lookup"><span data-stu-id="126ca-153">Test</span></span>        |
| <span data-ttu-id="126ca-154">Feature2</span><span class="sxs-lookup"><span data-stu-id="126ca-154">Feature2</span></span>  | <span data-ttu-id="126ca-155">Test2</span><span class="sxs-lookup"><span data-stu-id="126ca-155">Test2</span></span>       |



 

<span data-ttu-id="126ca-156">В этом случае необходимо убедиться, что по крайней мере одно из \[ \] свойств $componentkey имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="126ca-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="126ca-157">Однако каждое \[ свойство $componentkey \] в столбце Argument таблицы Verb ( \[ $comp 1 \] и \[ $comp 2 \] в приведенном выше примере) должно ссылаться на возможный компонент, входящий в состав расширения, связанного с командой.</span><span class="sxs-lookup"><span data-stu-id="126ca-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="126ca-158">Ссылка, например \[ $comp 3, приведет \] к появлению предупреждения от ICE69.</span><span class="sxs-lookup"><span data-stu-id="126ca-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="126ca-159">[Таблица AppID](appid-table.md) имеет схожую ситуацию с таблицей команд.</span><span class="sxs-lookup"><span data-stu-id="126ca-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="126ca-160">Он использует [таблицу классов](class-table.md) для ссылки на ее компонент.</span><span class="sxs-lookup"><span data-stu-id="126ca-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="126ca-161">В этом случае таблица AppId проверяется так же, как проверка Verb-Extension (теперь AppId-Class).</span><span class="sxs-lookup"><span data-stu-id="126ca-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="126ca-162">Столбец Argument таблицы класса проверяется как [ярлык](shortcut-table.md), [Реестр](registry-table.md)и аналогичные таблицы.</span><span class="sxs-lookup"><span data-stu-id="126ca-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="126ca-163">Таблица, используемая во время выполнения (только если она найдена)</span><span class="sxs-lookup"><span data-stu-id="126ca-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="126ca-164">инифиле</span><span class="sxs-lookup"><span data-stu-id="126ca-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="126ca-165">ремовеинифиле</span><span class="sxs-lookup"><span data-stu-id="126ca-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="126ca-166">Реестр</span><span class="sxs-lookup"><span data-stu-id="126ca-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="126ca-167">ремоверегистри</span><span class="sxs-lookup"><span data-stu-id="126ca-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="126ca-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="126ca-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="126ca-169">сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="126ca-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="126ca-170">Клавиша</span><span class="sxs-lookup"><span data-stu-id="126ca-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="126ca-171">Команда</span><span class="sxs-lookup"><span data-stu-id="126ca-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="126ca-172">Расширение</span><span class="sxs-lookup"><span data-stu-id="126ca-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="126ca-173">Класс</span><span class="sxs-lookup"><span data-stu-id="126ca-173">Class</span></span>](class-table.md)

[<span data-ttu-id="126ca-174">AppId</span><span class="sxs-lookup"><span data-stu-id="126ca-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="126ca-175">Среда</span><span class="sxs-lookup"><span data-stu-id="126ca-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="126ca-176">См. также</span><span class="sxs-lookup"><span data-stu-id="126ca-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="126ca-177">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="126ca-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



